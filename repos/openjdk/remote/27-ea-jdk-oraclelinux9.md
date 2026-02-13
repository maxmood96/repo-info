## `openjdk:27-ea-jdk-oraclelinux9`

```console
$ docker pull openjdk@sha256:e07c4160c0da5c0583ad70f97aa77ff14d45a8e951cd521eee828cb0033e3c25
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:27-ea-jdk-oraclelinux9` - linux; amd64

```console
$ docker pull openjdk@sha256:7ffd5c569e2fee18cac1aa82283e6ea2b70bd3f1c55f35963535803142fc91b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **313.9 MB (313924229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eeb9ce2016f14a98012d07c74b06b183b853b2c7cf7ac873776374dedbfcf202`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 05 Feb 2026 22:02:11 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Thu, 05 Feb 2026 22:02:11 GMT
CMD ["/bin/bash"]
# Fri, 13 Feb 2026 00:01:12 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 13 Feb 2026 00:01:22 GMT
ENV JAVA_HOME=/usr/java/openjdk-27
# Fri, 13 Feb 2026 00:01:22 GMT
ENV PATH=/usr/java/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 13 Feb 2026 00:01:22 GMT
ENV LANG=C.UTF-8
# Fri, 13 Feb 2026 00:01:22 GMT
ENV JAVA_VERSION=27-ea+8
# Fri, 13 Feb 2026 00:01:22 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/8/GPL/openjdk-27-ea+8_linux-x64_bin.tar.gz'; 			downloadSha256='26424619f5fc68be80026db27b8d73d0e36e791df4b4c4e8dbee4edae1f8ffeb'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/8/GPL/openjdk-27-ea+8_linux-aarch64_bin.tar.gz'; 			downloadSha256='7ca3627abde323298007e3644968cd30d4363d289840c83bd0b8b49ccd84da51'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 13 Feb 2026 00:01:22 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:4f37333d1be658a226cdafd622c7bda0a95abbcb999c29a571136add51950044`  
		Last Modified: Thu, 05 Feb 2026 22:02:22 GMT  
		Size: 47.3 MB (47307542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed62308835fcd9ba29f3ee8279b8e2a69dfb9a32da4a90f4fa095f8bec734b71`  
		Last Modified: Fri, 13 Feb 2026 00:01:45 GMT  
		Size: 38.3 MB (38300007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bd3016dc9663456098379bac7a469648029831c2cf1542c2a87e1b6a1a8ca04`  
		Last Modified: Fri, 13 Feb 2026 00:01:48 GMT  
		Size: 228.3 MB (228316680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-jdk-oraclelinux9` - unknown; unknown

```console
$ docker pull openjdk@sha256:9a38664240d1bdf58e2e2dda9b7d57aaad9e6c2d6f06095c8b35cf83a20c76cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3672597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b20e07e2fb9b434d834b1c1adbed0361ef7652062bbfc4288d44a671786421c`

```dockerfile
```

-	Layers:
	-	`sha256:2eeb08887711ff7d10f071227dcc5bc9ae7387780c8ff41ca70540b02764ae28`  
		Last Modified: Fri, 13 Feb 2026 00:01:44 GMT  
		Size: 3.7 MB (3654783 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e313ef4689053b44a260898f84ce0cde8fd72670dd3ec3dbc6cffd0f20e63807`  
		Last Modified: Fri, 13 Feb 2026 00:01:43 GMT  
		Size: 17.8 KB (17814 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:27-ea-jdk-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:692ec6aec373cfd3cba5405c5f3c5a4f6ccfa593de48b3cfbe3d22a11d5caf58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.9 MB (310859409 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84176627e6750ac19f2a7008640905c44dae4592f1397c63a9acc1bef1421fe0`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 05 Feb 2026 22:01:48 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Thu, 05 Feb 2026 22:01:48 GMT
CMD ["/bin/bash"]
# Fri, 13 Feb 2026 00:03:00 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 13 Feb 2026 00:03:10 GMT
ENV JAVA_HOME=/usr/java/openjdk-27
# Fri, 13 Feb 2026 00:03:10 GMT
ENV PATH=/usr/java/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 13 Feb 2026 00:03:10 GMT
ENV LANG=C.UTF-8
# Fri, 13 Feb 2026 00:03:10 GMT
ENV JAVA_VERSION=27-ea+8
# Fri, 13 Feb 2026 00:03:10 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/8/GPL/openjdk-27-ea+8_linux-x64_bin.tar.gz'; 			downloadSha256='26424619f5fc68be80026db27b8d73d0e36e791df4b4c4e8dbee4edae1f8ffeb'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/8/GPL/openjdk-27-ea+8_linux-aarch64_bin.tar.gz'; 			downloadSha256='7ca3627abde323298007e3644968cd30d4363d289840c83bd0b8b49ccd84da51'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 13 Feb 2026 00:03:10 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:bdaccdb6a2d14a7ee18a3d1ff57e3f6bd4e826bf7bda3d4995e73942beb6ca3a`  
		Last Modified: Thu, 05 Feb 2026 22:02:00 GMT  
		Size: 45.9 MB (45903410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b59ed6c86a9d27ae6e46df6cbddda311aed05fac91b3e5ddb4108594b7e45a7`  
		Last Modified: Fri, 13 Feb 2026 00:03:33 GMT  
		Size: 38.7 MB (38697267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77dbccd2e801f36786143c3c3eb42386572ce860f02583c64127cfa8627f889c`  
		Last Modified: Fri, 13 Feb 2026 00:03:36 GMT  
		Size: 226.3 MB (226258732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-jdk-oraclelinux9` - unknown; unknown

```console
$ docker pull openjdk@sha256:3af4c8f0de418047923189a109a5edba08c186b115edc14bbf24fdac86da7926
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3670501 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f75340996dc117079cdf8e0f593863bd5db1f1b17d9413f46dd1ce34e46a7c4e`

```dockerfile
```

-	Layers:
	-	`sha256:496bd15a4efe4f4e2d8077a37148afb3034583024de9fccdc57f99ed4346dd53`  
		Last Modified: Fri, 13 Feb 2026 00:03:31 GMT  
		Size: 3.7 MB (3652473 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aa0213bd911eaa4b30eeb31c4e92285c3b044c4c4468c8f29c123114b447664c`  
		Last Modified: Fri, 13 Feb 2026 00:03:31 GMT  
		Size: 18.0 KB (18028 bytes)  
		MIME: application/vnd.in-toto+json
