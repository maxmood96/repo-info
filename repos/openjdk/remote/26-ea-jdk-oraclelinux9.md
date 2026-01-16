## `openjdk:26-ea-jdk-oraclelinux9`

```console
$ docker pull openjdk@sha256:49195a3ff7054ec9bff7f35ef8ca30b0175f2c85b5138f2f2949bd9cf3f52df4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:26-ea-jdk-oraclelinux9` - linux; amd64

```console
$ docker pull openjdk@sha256:320a0f6e234d7851ebb9fbe58497a01739579abcdd0dfae920c7cbaca612a4d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **313.5 MB (313459024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c255d61fb2e942efe002ac17471635926b197e02ce58a3f0d301297886128845`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 06 Jan 2026 18:24:14 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 06 Jan 2026 18:24:14 GMT
CMD ["/bin/bash"]
# Mon, 12 Jan 2026 20:07:44 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Mon, 12 Jan 2026 20:07:52 GMT
ENV JAVA_HOME=/usr/java/openjdk-26
# Mon, 12 Jan 2026 20:07:52 GMT
ENV PATH=/usr/java/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 12 Jan 2026 20:07:52 GMT
ENV LANG=C.UTF-8
# Mon, 12 Jan 2026 20:07:52 GMT
ENV JAVA_VERSION=26-ea+30
# Mon, 12 Jan 2026 20:07:52 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/30/GPL/openjdk-26-ea+30_linux-x64_bin.tar.gz'; 			downloadSha256='300f7c67876f470e3ddacfd75be07c3c92812847b43933eb3600e258a9662e2d'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/30/GPL/openjdk-26-ea+30_linux-aarch64_bin.tar.gz'; 			downloadSha256='466961f9222d91364dbc631bb8c76216dbecaf025464f0189b3acc96dd516a96'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Mon, 12 Jan 2026 20:07:52 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:ad9d782f3f8782ebff0dd18c48de1ae7dd7e8c7e8b207aee14fd087419cb908f`  
		Last Modified: Tue, 06 Jan 2026 18:24:34 GMT  
		Size: 47.3 MB (47316998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6abee3a5dd93a8daa268eb1a2db712584c05ca9e6d556ad2b27d56b7e1b0c0d3`  
		Last Modified: Mon, 12 Jan 2026 20:08:27 GMT  
		Size: 38.3 MB (38300121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:956c45fee91ae172f1df90fc8314c47f72b4beb8078d8b898505c3254562d262`  
		Last Modified: Mon, 12 Jan 2026 20:08:36 GMT  
		Size: 227.8 MB (227841905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-ea-jdk-oraclelinux9` - unknown; unknown

```console
$ docker pull openjdk@sha256:edd5459df131c63c5843c8a226b65fb6d1b292e4844ca2a0b5229e66c293cda7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3673206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0c3ce479afe84384f3ac290882216b534f3ac29f1e79874d9ad987b55697625`

```dockerfile
```

-	Layers:
	-	`sha256:13952054b7071ca1b3705dc16142a9a6198b447c0769fcd1bc1f5c277bbcef43`  
		Last Modified: Mon, 12 Jan 2026 22:23:29 GMT  
		Size: 3.7 MB (3655367 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:939363c45740d0940d13c66e1a1ed0b5805da290c8fd39f7749f9dec296180da`  
		Last Modified: Mon, 12 Jan 2026 22:23:30 GMT  
		Size: 17.8 KB (17839 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:26-ea-jdk-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:1587d7e453782b0130addbdf4f193cce87067c48f5a24583f396855a371ebe3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.4 MB (310361052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f31f25930eb1a49bddcada8f97f09e33a865068499c36355f34781c1122e861`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 06 Jan 2026 18:24:32 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 06 Jan 2026 18:24:32 GMT
CMD ["/bin/bash"]
# Mon, 12 Jan 2026 20:08:21 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Mon, 12 Jan 2026 20:08:32 GMT
ENV JAVA_HOME=/usr/java/openjdk-26
# Mon, 12 Jan 2026 20:08:32 GMT
ENV PATH=/usr/java/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 12 Jan 2026 20:08:32 GMT
ENV LANG=C.UTF-8
# Mon, 12 Jan 2026 20:08:32 GMT
ENV JAVA_VERSION=26-ea+30
# Mon, 12 Jan 2026 20:08:32 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/30/GPL/openjdk-26-ea+30_linux-x64_bin.tar.gz'; 			downloadSha256='300f7c67876f470e3ddacfd75be07c3c92812847b43933eb3600e258a9662e2d'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/30/GPL/openjdk-26-ea+30_linux-aarch64_bin.tar.gz'; 			downloadSha256='466961f9222d91364dbc631bb8c76216dbecaf025464f0189b3acc96dd516a96'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Mon, 12 Jan 2026 20:08:32 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:0e1814e660b35a8d0d1c9103cf854824718c8d9101e743cca376efd3f99eb9a1`  
		Last Modified: Tue, 06 Jan 2026 18:24:56 GMT  
		Size: 45.9 MB (45905540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66e19be33da1d308e86c3dcd7d762957b21c4b9327cdca648d8f1338e054276b`  
		Last Modified: Mon, 12 Jan 2026 20:09:10 GMT  
		Size: 38.7 MB (38696850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:976fa1f0f82887717328bb21403bb94effbacae7a40578a5764e6a575a6f1a59`  
		Last Modified: Mon, 12 Jan 2026 20:09:30 GMT  
		Size: 225.8 MB (225758662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-ea-jdk-oraclelinux9` - unknown; unknown

```console
$ docker pull openjdk@sha256:0c562b7d60e6e82eeb00a4fd3fbe411ece7b52e4e77474548ead721c1cb9dfc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3671111 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1403805c8f3b7df06eb842b896dd664f9c3cfdc5fc980efc8eeb2cd897eceaad`

```dockerfile
```

-	Layers:
	-	`sha256:a3cb479debde05ec0451b7b0fe7182843894b42555ebbb45f97be136e5446493`  
		Last Modified: Mon, 12 Jan 2026 22:23:42 GMT  
		Size: 3.7 MB (3653057 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f612648aa72f321e09b056d013b1c34b105e0e2873b5afbd35d75030213f1859`  
		Last Modified: Mon, 12 Jan 2026 22:23:43 GMT  
		Size: 18.1 KB (18054 bytes)  
		MIME: application/vnd.in-toto+json
