## `openjdk:27-ea-jdk-bookworm`

```console
$ docker pull openjdk@sha256:c4703738f01c06d40b9fe3cdce0ded2cfd3eb75da67afebb665bf6c3df049c22
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:27-ea-jdk-bookworm` - linux; amd64

```console
$ docker pull openjdk@sha256:caedd6fad2edb95e1ac7d64204c26b435801dd5d3a1baafb206fece4151f1f0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **381.0 MB (380966634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb939bf4bedf6c944ea1df2c15f8dcc2301b5c65e581ce77e06c821fd9536804`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 00:42:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 02:24:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 03:17:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 03:18:01 GMT
ENV JAVA_HOME=/usr/local/openjdk-27
# Thu, 11 Jun 2026 03:18:01 GMT
ENV PATH=/usr/local/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jun 2026 03:18:01 GMT
ENV LANG=C.UTF-8
# Thu, 11 Jun 2026 03:18:01 GMT
ENV JAVA_VERSION=27-ea+25
# Thu, 11 Jun 2026 03:18:01 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/25/GPL/openjdk-27-ea+25_linux-x64_bin.tar.gz'; 			downloadSha256='6287dc1b8b810fc6fb0ecf2ff0f15464e7bbd5b44c45008588224072bbfbaa87'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/25/GPL/openjdk-27-ea+25_linux-aarch64_bin.tar.gz'; 			downloadSha256='6f13903699316f8ee6089a0551ef28686b3bae5b195a98cc4051b365819396cb'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Thu, 11 Jun 2026 03:18:01 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:01cedcff86f879d042805360ecba268802bec3d8201484ff3ec54f4250a2d3b7`  
		Last Modified: Wed, 10 Jun 2026 23:39:39 GMT  
		Size: 48.5 MB (48502042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4da31edd9efdb812e66d13819903973ea6b188d2e7358547676d33d1e3f706f2`  
		Last Modified: Thu, 11 Jun 2026 00:42:23 GMT  
		Size: 24.0 MB (24044000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fbaeeb62b9d03a1204b85c3b257aa3e1ce2c4ccfeea479fb2e659211019c29d`  
		Last Modified: Thu, 11 Jun 2026 02:24:43 GMT  
		Size: 64.4 MB (64404116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fe69800f8f7b79898ed632f6593a9fafa54fc60054ada161a67b1f1f1826fb2`  
		Last Modified: Thu, 11 Jun 2026 03:18:27 GMT  
		Size: 16.9 MB (16946479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dc4cbad8795c020b89b8e4e78ecb098bf41abf203f93078e6cfaae6acaeedc1`  
		Last Modified: Thu, 11 Jun 2026 03:18:32 GMT  
		Size: 227.1 MB (227069997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-jdk-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:a1491b30544b3e444aaf2f20601da4b5a36f98f1071dd0f309bed16ba4896e3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 MB (8684313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a1e05216519696d57eef708c03cdef7229e72c60a9fe5d322381a575e17830f`

```dockerfile
```

-	Layers:
	-	`sha256:2adca62e93afe7b6b4f4472ff6ca0c820c322043af1f4e4747fd4756e68fcd03`  
		Last Modified: Thu, 11 Jun 2026 03:18:26 GMT  
		Size: 8.7 MB (8666374 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:375f631583ea211928e172db7b33f8ab15720490b95c14d78b45968555352cd8`  
		Last Modified: Thu, 11 Jun 2026 03:18:26 GMT  
		Size: 17.9 KB (17939 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:27-ea-jdk-bookworm` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:b2bd0fe0bf7be4f0cf97467e468b102011a0275a2cbf6af95d80c526ded3f0a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **379.3 MB (379266334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23765cf953813eb50fb6604cdefdd7b14362678a5f264296f8e07be9bc68e870`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 00:43:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 02:24:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 03:17:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 03:17:56 GMT
ENV JAVA_HOME=/usr/local/openjdk-27
# Thu, 11 Jun 2026 03:17:56 GMT
ENV PATH=/usr/local/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jun 2026 03:17:56 GMT
ENV LANG=C.UTF-8
# Thu, 11 Jun 2026 03:17:56 GMT
ENV JAVA_VERSION=27-ea+25
# Thu, 11 Jun 2026 03:17:56 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/25/GPL/openjdk-27-ea+25_linux-x64_bin.tar.gz'; 			downloadSha256='6287dc1b8b810fc6fb0ecf2ff0f15464e7bbd5b44c45008588224072bbfbaa87'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/25/GPL/openjdk-27-ea+25_linux-aarch64_bin.tar.gz'; 			downloadSha256='6f13903699316f8ee6089a0551ef28686b3bae5b195a98cc4051b365819396cb'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Thu, 11 Jun 2026 03:17:56 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:c847f328095fb083f4a22895b90fe4226efa6458ac57362b64b6e5d99da9e4a3`  
		Last Modified: Wed, 10 Jun 2026 23:39:28 GMT  
		Size: 48.4 MB (48389016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f511b4c80a6e453785fbcd573c1bf1cb986c4e8d43ed4500ad1ac9a4719762b`  
		Last Modified: Thu, 11 Jun 2026 00:43:56 GMT  
		Size: 23.6 MB (23613296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b715a6712db064e97302c819acd7a39c0c72f8a315ff83c6ad1c27bfa1b275e`  
		Last Modified: Thu, 11 Jun 2026 02:25:01 GMT  
		Size: 64.5 MB (64487878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f6cadc0508db832b359cd7e4b98fe4a1fa83608e2ebaf4aede1158964146b20`  
		Last Modified: Thu, 11 Jun 2026 03:18:22 GMT  
		Size: 17.7 MB (17730222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d50bc43fe12917bc5d1dcd446fa17b3936bcb486742ac4c5324860872987b28`  
		Last Modified: Thu, 11 Jun 2026 03:18:27 GMT  
		Size: 225.0 MB (225045922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-jdk-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:cf0047cccd4414bb86f07b18b8e6752bb927a1c2a46564e98397e7b51c391adf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8821276 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74182c5369e3990604a407a17439dfcebcffccc6f5eb6e1785f47690bd0cbb3d`

```dockerfile
```

-	Layers:
	-	`sha256:7004fc982649f884d79f410cc83abfad6ca06fd13123ef92ca82b3dc8844f2ab`  
		Last Modified: Thu, 11 Jun 2026 03:18:22 GMT  
		Size: 8.8 MB (8803219 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:45719b8676d76cf3e166affc70e6672cb706a5bafef9fd1b5bcdddf54e2c847c`  
		Last Modified: Thu, 11 Jun 2026 03:18:21 GMT  
		Size: 18.1 KB (18057 bytes)  
		MIME: application/vnd.in-toto+json
