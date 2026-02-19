## `openjdk:26-rc-oracle`

```console
$ docker pull openjdk@sha256:9c08ecc47c580fc1909d08248d917c6ad9e64fae1ae582be460b098510546a26
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:26-rc-oracle` - linux; amd64

```console
$ docker pull openjdk@sha256:7297bc0750cde943b19f4e8ccbc0e6b3ca968c608fc5a4d9fd567edbe1a12aa3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **313.5 MB (313542163 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4be149be6d870ec2d926bddccfaa99cc9f41a847c1a8385aa809694c9924afc`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 19 Feb 2026 19:11:41 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Thu, 19 Feb 2026 19:11:41 GMT
CMD ["/bin/bash"]
# Thu, 19 Feb 2026 19:38:20 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Thu, 19 Feb 2026 19:38:29 GMT
ENV JAVA_HOME=/usr/java/openjdk-26
# Thu, 19 Feb 2026 19:38:29 GMT
ENV PATH=/usr/java/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 19 Feb 2026 19:38:29 GMT
ENV LANG=C.UTF-8
# Thu, 19 Feb 2026 19:38:29 GMT
ENV JAVA_VERSION=26
# Thu, 19 Feb 2026 19:38:29 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/GA/jdk26/c3cc523845074aa0af4f5e1e1ed4151d/35/GPL/openjdk-26_linux-x64_bin.tar.gz'; 			downloadSha256='83c78367f8c81257beef72aca4bbbf8e6dac8ca2b3a4546a85879a09e6e4e128'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/GA/jdk26/c3cc523845074aa0af4f5e1e1ed4151d/35/GPL/openjdk-26_linux-aarch64_bin.tar.gz'; 			downloadSha256='403ccf451e88d0be9e1dec129fcb9318de9752121e0eb92dfa9a8cf06f249007'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Thu, 19 Feb 2026 19:38:29 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:74a8e4bbd9fe8a9fb7df9f028398fc37d20efc1cde6bf66eeeabef7755e5f5fe`  
		Last Modified: Thu, 19 Feb 2026 19:11:53 GMT  
		Size: 47.3 MB (47308871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5f15c9ff2a00ce61779592faebfb95ed52f9cb90c301b95e02b59d80be6ed56`  
		Last Modified: Thu, 19 Feb 2026 19:38:53 GMT  
		Size: 38.3 MB (38296685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70044eb955e310c1a90e03aba26215ca051dc9800cea2c59a35eb746fa0cd56f`  
		Last Modified: Thu, 19 Feb 2026 19:38:59 GMT  
		Size: 227.9 MB (227936607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-rc-oracle` - unknown; unknown

```console
$ docker pull openjdk@sha256:81279e38a9a214f5c6de48bef556ed3909a0e1e8ce6797a17f6a295dceaf2d29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3670092 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41c9ea5d1a325e071271c5ac68f900127a6206d905f29e48b278e37972063e7c`

```dockerfile
```

-	Layers:
	-	`sha256:63ea3a9e6d7c2a917de15d61eebb2482e1b7f2fba9fab02989b9a9e424c99d7c`  
		Last Modified: Thu, 19 Feb 2026 19:38:52 GMT  
		Size: 3.7 MB (3654117 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3cb436a74bbbdafe3e865b7509fc31f048d89d07337a5951fb2f16ea06209d0b`  
		Last Modified: Thu, 19 Feb 2026 19:38:51 GMT  
		Size: 16.0 KB (15975 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:26-rc-oracle` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:08023c7307aae5e22851f24fd85c3d3ee27281f1107d7d83aa70cf3420dc687d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.5 MB (310459546 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c0e558bcc5bc7ae9e8023fa2423dcca60a857573c97fff726da2592f27b9770`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 19 Feb 2026 19:06:57 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Thu, 19 Feb 2026 19:06:57 GMT
CMD ["/bin/bash"]
# Thu, 19 Feb 2026 19:37:50 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Thu, 19 Feb 2026 19:38:01 GMT
ENV JAVA_HOME=/usr/java/openjdk-26
# Thu, 19 Feb 2026 19:38:01 GMT
ENV PATH=/usr/java/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 19 Feb 2026 19:38:01 GMT
ENV LANG=C.UTF-8
# Thu, 19 Feb 2026 19:38:01 GMT
ENV JAVA_VERSION=26
# Thu, 19 Feb 2026 19:38:01 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/GA/jdk26/c3cc523845074aa0af4f5e1e1ed4151d/35/GPL/openjdk-26_linux-x64_bin.tar.gz'; 			downloadSha256='83c78367f8c81257beef72aca4bbbf8e6dac8ca2b3a4546a85879a09e6e4e128'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/GA/jdk26/c3cc523845074aa0af4f5e1e1ed4151d/35/GPL/openjdk-26_linux-aarch64_bin.tar.gz'; 			downloadSha256='403ccf451e88d0be9e1dec129fcb9318de9752121e0eb92dfa9a8cf06f249007'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Thu, 19 Feb 2026 19:38:01 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:482e8d56575a6fbe539cfb44150fa96593766f3af0610165cb5c8a63fa68d8db`  
		Last Modified: Thu, 19 Feb 2026 19:07:09 GMT  
		Size: 45.9 MB (45901980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aba169c606464ec011ece3abb80fcb27b052386c7535df541d2aa96937b5cdeb`  
		Last Modified: Thu, 19 Feb 2026 19:38:25 GMT  
		Size: 38.7 MB (38693389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0af0997b4a308402c88eb0b0ffa16502d30e40641d49d28fbfa202fa1f2ce8c8`  
		Last Modified: Thu, 19 Feb 2026 19:38:33 GMT  
		Size: 225.9 MB (225864177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-rc-oracle` - unknown; unknown

```console
$ docker pull openjdk@sha256:178a0b82f8ece9098436781c21922ec392a83ac028ea91ef7148efa2af30eb30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3667853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8366d442a33cf3921c59c2d30e4baab277443933714b3e0cbe270ad734d2e4d7`

```dockerfile
```

-	Layers:
	-	`sha256:ae4ebfd0260ccb2a22ef3c87d3ddd58e6e6c90a9d07a0c05e200348c09b113a8`  
		Last Modified: Thu, 19 Feb 2026 19:38:24 GMT  
		Size: 3.7 MB (3651735 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e2b76eafa9acc79c8568bba963b21f39c855f0bd182eb3dcca9380c2cf638c12`  
		Last Modified: Thu, 19 Feb 2026 19:38:24 GMT  
		Size: 16.1 KB (16118 bytes)  
		MIME: application/vnd.in-toto+json
