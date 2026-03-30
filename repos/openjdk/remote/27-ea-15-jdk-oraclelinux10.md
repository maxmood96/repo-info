## `openjdk:27-ea-15-jdk-oraclelinux10`

```console
$ docker pull openjdk@sha256:c809626ab9570189a03cb9733b8cd813f3f98d74e8a31e689899878a1ae78f1a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:27-ea-15-jdk-oraclelinux10` - linux; amd64

```console
$ docker pull openjdk@sha256:fc102b3599f82aef8c0c08ccda51328786551ac15a748203723a3dfb4bfb41a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **309.2 MB (309235654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f1a5f087457518e723ac3e1448874c384d15837a762fdd7633e7cfd00a16819`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 27 Mar 2026 00:16:42 GMT
ADD oraclelinux-10-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 27 Mar 2026 00:16:42 GMT
CMD ["/bin/bash"]
# Mon, 30 Mar 2026 17:50:41 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Mon, 30 Mar 2026 17:50:54 GMT
ENV JAVA_HOME=/usr/java/openjdk-27
# Mon, 30 Mar 2026 17:50:54 GMT
ENV PATH=/usr/java/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 30 Mar 2026 17:50:54 GMT
ENV LANG=C.UTF-8
# Mon, 30 Mar 2026 17:50:54 GMT
ENV JAVA_VERSION=27-ea+15
# Mon, 30 Mar 2026 17:50:54 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/15/GPL/openjdk-27-ea+15_linux-x64_bin.tar.gz'; 			downloadSha256='5cfe1cf2f5d5ebbcdd826c7298fbabc42d656edbe9544c74b1ee84df6e5326a7'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/15/GPL/openjdk-27-ea+15_linux-aarch64_bin.tar.gz'; 			downloadSha256='ab3f14d81c06590facec1138b71b55a7f64d47c0e0845113c9a8ecd4be6751bb'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Mon, 30 Mar 2026 17:50:54 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1101a6a16bdd51aef6dda35e785dca1d7934d2937fdc0c8dfc0f002ced99f85a`  
		Last Modified: Fri, 27 Mar 2026 00:16:52 GMT  
		Size: 43.1 MB (43068827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04566866e4406a94bca5c57b49bc3c6eeecf76bfb58cd656b6499f4f552ca468`  
		Last Modified: Mon, 30 Mar 2026 17:51:15 GMT  
		Size: 37.7 MB (37679216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2734fdb26ab0515b0fbde7154045fab3e9451cd5a7d185a1fc697da5fa25d96`  
		Last Modified: Mon, 30 Mar 2026 17:51:18 GMT  
		Size: 228.5 MB (228487611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-15-jdk-oraclelinux10` - unknown; unknown

```console
$ docker pull openjdk@sha256:ee462b87fc0b98aaf2fb5e004292089789f6954e1632256558c4954948cbdd41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2386197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79045d1dd241a4cdd01691a8ba21c5ee926084b775cc1999afdc2029692fcca5`

```dockerfile
```

-	Layers:
	-	`sha256:41a4faebc00cb6387b215190f55c3d000e06f50ead8572f95e51f67e08442ebf`  
		Last Modified: Mon, 30 Mar 2026 17:51:13 GMT  
		Size: 2.4 MB (2368347 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4ea572b15378bec13b34daa460f49cdd5f42d27662e7fb804afdc5ccbf763ce8`  
		Last Modified: Mon, 30 Mar 2026 17:51:13 GMT  
		Size: 17.9 KB (17850 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:27-ea-15-jdk-oraclelinux10` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:5bcfb6381d5825624999c20f210403081ab6f2c2fa4c602df3c2f2ed49fb8947
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.6 MB (305616742 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0aa8022be54f3d54bfc30ef209027ee0fd00f3ef52f45caee251b5961ff93f2e`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 27 Mar 2026 00:16:42 GMT
ADD oraclelinux-10-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 27 Mar 2026 00:16:42 GMT
CMD ["/bin/bash"]
# Mon, 30 Mar 2026 17:48:19 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Mon, 30 Mar 2026 17:48:37 GMT
ENV JAVA_HOME=/usr/java/openjdk-27
# Mon, 30 Mar 2026 17:48:37 GMT
ENV PATH=/usr/java/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 30 Mar 2026 17:48:37 GMT
ENV LANG=C.UTF-8
# Mon, 30 Mar 2026 17:48:37 GMT
ENV JAVA_VERSION=27-ea+15
# Mon, 30 Mar 2026 17:48:37 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/15/GPL/openjdk-27-ea+15_linux-x64_bin.tar.gz'; 			downloadSha256='5cfe1cf2f5d5ebbcdd826c7298fbabc42d656edbe9544c74b1ee84df6e5326a7'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/15/GPL/openjdk-27-ea+15_linux-aarch64_bin.tar.gz'; 			downloadSha256='ab3f14d81c06590facec1138b71b55a7f64d47c0e0845113c9a8ecd4be6751bb'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Mon, 30 Mar 2026 17:48:37 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f3db22c05661dd4dd65ed2c3add4946b3292ef86d7a62c06699ee25367fc2e1b`  
		Last Modified: Fri, 27 Mar 2026 00:16:52 GMT  
		Size: 41.5 MB (41474500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24b9996a7d6cf0baeeb6abf8c380afe5a522e4ed6cedf273ff0d644e77b1500e`  
		Last Modified: Mon, 30 Mar 2026 17:48:59 GMT  
		Size: 37.7 MB (37688022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c9d342d1ed837abd9cf84381f824c735486fd87e35c341f3e314179ac8e2b12`  
		Last Modified: Mon, 30 Mar 2026 17:49:03 GMT  
		Size: 226.5 MB (226454220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-15-jdk-oraclelinux10` - unknown; unknown

```console
$ docker pull openjdk@sha256:c0f28340314133404e46434bf35a1908d88c728343585ff68dd346e2f4459d44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2385940 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd0706908a145b149499d7b1e176612cd2f820ed399f4dd7c3b4c9fb116d7ead`

```dockerfile
```

-	Layers:
	-	`sha256:b900ef566371af3d0093e85f642824452abf31c4f9afed8a28c8e680a71996eb`  
		Last Modified: Mon, 30 Mar 2026 17:48:58 GMT  
		Size: 2.4 MB (2367875 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:deba7452f443608845f5b79545bbea23bdbb55cd807c6ed87184e099409e6790`  
		Last Modified: Mon, 30 Mar 2026 17:48:58 GMT  
		Size: 18.1 KB (18065 bytes)  
		MIME: application/vnd.in-toto+json
