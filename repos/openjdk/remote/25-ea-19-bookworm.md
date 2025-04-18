## `openjdk:25-ea-19-bookworm`

```console
$ docker pull openjdk@sha256:e1ad6f8acb7e3c9d816b40ee415ccc022dc0e02bf112e4b49ed7d3595086b9a8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:25-ea-19-bookworm` - linux; amd64

```console
$ docker pull openjdk@sha256:3668a788f56e39cd6e41deaf06e164a5bf30b85968ee49ae68a53c978da3816a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **366.3 MB (366338038 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:728b795b59fdf3f30e872e86a93715dbc68c2e234e2b5a2bb9accded845ac48e`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1743984000'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 18 Apr 2025 00:48:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 18 Apr 2025 00:48:12 GMT
ENV JAVA_HOME=/usr/local/openjdk-25
# Fri, 18 Apr 2025 00:48:12 GMT
ENV PATH=/usr/local/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 18 Apr 2025 00:48:12 GMT
ENV LANG=C.UTF-8
# Fri, 18 Apr 2025 00:48:12 GMT
ENV JAVA_VERSION=25-ea+19
# Fri, 18 Apr 2025 00:48:12 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/19/GPL/openjdk-25-ea+19_linux-x64_bin.tar.gz'; 			downloadSha256='5d10a87dcb2a162df9f7ab0c97cc77eff71c53ad442cbf40cce33b8ab6ab117a'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/19/GPL/openjdk-25-ea+19_linux-aarch64_bin.tar.gz'; 			downloadSha256='1324cfa105b4ce10e2ab854c20d7e1a4eda81fb6a1df35dacadc8d65b0b59351'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 18 Apr 2025 00:48:12 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:23b7d26ef1d294256da0d70ce374277b9aab5ca683015073316005cb63d33849`  
		Last Modified: Tue, 08 Apr 2025 00:22:55 GMT  
		Size: 48.5 MB (48490541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07d1b5af933d2dfc3d0dd509d6e20534825e4a537f7b006a6cb5b8e5a1f20905`  
		Last Modified: Tue, 08 Apr 2025 01:24:20 GMT  
		Size: 24.0 MB (24011090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1eb98adba0eb44a2e4facf9ca3626a4a66feedd0dd56d159cca90a35205744e7`  
		Last Modified: Tue, 08 Apr 2025 02:13:59 GMT  
		Size: 64.4 MB (64396468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f8820eff70df584794fac315d5eabd2e8098d5a37cdf648925615e5a8b5f15a`  
		Last Modified: Fri, 18 Apr 2025 18:37:50 GMT  
		Size: 16.9 MB (16943439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6954906995a4c5feb5c89fbd04a2659b79fb9102a015df6d5446a02d97fa5ba2`  
		Last Modified: Fri, 18 Apr 2025 18:37:53 GMT  
		Size: 212.5 MB (212496500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-ea-19-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:6740cfc5a52c215cd561393b249962c44e33e0c2490748bb33032cbad765dea9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.5 MB (8451953 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7ee4db8537e2ee45fb2f7f7eeaa39d7395fa4b638e7809b9ce1dbc95ded0bfa`

```dockerfile
```

-	Layers:
	-	`sha256:7c35f88d09d95743e6598bc6d61ca4d666ec3f7347c0cd07a68b6b2987de0229`  
		Last Modified: Fri, 18 Apr 2025 18:37:49 GMT  
		Size: 8.4 MB (8433335 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:76a5e325d8c3b48c52650fff3aa32cd00648dc503ee65c02a41c1bd69bc5a041`  
		Last Modified: Fri, 18 Apr 2025 18:37:49 GMT  
		Size: 18.6 KB (18618 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:25-ea-19-bookworm` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:cff814bf3a1f38981b685d107cf5b647b0384666a6590191bbcf4b60cfad37a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **364.3 MB (364267513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8c2731bab17625536fb3b429c5399d5cf5a1c2cb605832cbf399b44208607cb`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1743984000'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 18 Apr 2025 00:48:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 18 Apr 2025 00:48:12 GMT
ENV JAVA_HOME=/usr/local/openjdk-25
# Fri, 18 Apr 2025 00:48:12 GMT
ENV PATH=/usr/local/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 18 Apr 2025 00:48:12 GMT
ENV LANG=C.UTF-8
# Fri, 18 Apr 2025 00:48:12 GMT
ENV JAVA_VERSION=25-ea+19
# Fri, 18 Apr 2025 00:48:12 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/19/GPL/openjdk-25-ea+19_linux-x64_bin.tar.gz'; 			downloadSha256='5d10a87dcb2a162df9f7ab0c97cc77eff71c53ad442cbf40cce33b8ab6ab117a'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/19/GPL/openjdk-25-ea+19_linux-aarch64_bin.tar.gz'; 			downloadSha256='1324cfa105b4ce10e2ab854c20d7e1a4eda81fb6a1df35dacadc8d65b0b59351'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 18 Apr 2025 00:48:12 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:71daa2c787b0984bbf3b93b60686fc9fe305d28e833914019b2745ab9f36730e`  
		Last Modified: Tue, 08 Apr 2025 00:22:46 GMT  
		Size: 48.3 MB (48327469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d81c64672754c46e5d99e385c8f3283bec2060a79ad7dacdb2f5ce904caa401`  
		Last Modified: Tue, 08 Apr 2025 06:03:14 GMT  
		Size: 23.5 MB (23544339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebf144460616b42eb1462fd80a5e1909e578b1e1f7285b185e468ba2b01308b9`  
		Last Modified: Tue, 08 Apr 2025 12:18:06 GMT  
		Size: 64.4 MB (64355780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3c6f8c583e350c4c0560ef0654dff7fbc9a5e71b683b62b9d74ac05195f4329`  
		Last Modified: Mon, 14 Apr 2025 23:01:05 GMT  
		Size: 17.7 MB (17727052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d49c791eb7c673013125a0bc067337cab27ee72867e58d82868b4f43bc04723`  
		Last Modified: Fri, 18 Apr 2025 18:39:22 GMT  
		Size: 210.3 MB (210312873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-ea-19-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:cbc2ed38b288e85f545a01aa54d63b1cbf9d30d33f14a118cdddd5fbd2664d94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.6 MB (8588964 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:822ac84d3642f1b91ff33069f9cf0fb89c6317da43ddfcaf68ccdafa4899a495`

```dockerfile
```

-	Layers:
	-	`sha256:daf822c70e43cb3f94b8ef385b024ae39b35cc652ae2fb1d8e88e39e52abdd88`  
		Last Modified: Fri, 18 Apr 2025 18:39:17 GMT  
		Size: 8.6 MB (8570203 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c17012719806f5ab40612ed8d81179a30dfbd1a069efb995e3ffc7db658b2063`  
		Last Modified: Fri, 18 Apr 2025 18:39:16 GMT  
		Size: 18.8 KB (18761 bytes)  
		MIME: application/vnd.in-toto+json
