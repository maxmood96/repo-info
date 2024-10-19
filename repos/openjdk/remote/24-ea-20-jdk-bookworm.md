## `openjdk:24-ea-20-jdk-bookworm`

```console
$ docker pull openjdk@sha256:47717ec0c85b2bff89e7d12cd84c4fa1d7b230beed9ce6741df4f9a2959a2e05
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `openjdk:24-ea-20-jdk-bookworm` - linux; amd64

```console
$ docker pull openjdk@sha256:c3eac0e3155f63bb69e494ee250ae6f83598807b15c7478a6d004b4ab66c7483
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **367.5 MB (367481198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1177d7bceafbc90d1ab7dca124f03854160f1d408ac10e3fe785c868b4e536b4`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD file:b4987bca8c4c4c640d6b71dcccfd7172b44771e0f851a47d05c00c2bdcd204f6 in / 
# Wed, 10 May 2023 23:29:59 GMT
CMD ["bash"]
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 18 Oct 2024 00:48:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 18 Oct 2024 00:48:11 GMT
ENV JAVA_HOME=/usr/local/openjdk-24
# Fri, 18 Oct 2024 00:48:11 GMT
ENV PATH=/usr/local/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 18 Oct 2024 00:48:11 GMT
ENV LANG=C.UTF-8
# Fri, 18 Oct 2024 00:48:11 GMT
ENV JAVA_VERSION=24-ea+20
# Fri, 18 Oct 2024 00:48:11 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/20/GPL/openjdk-24-ea+20_linux-x64_bin.tar.gz'; 			downloadSha256='b7a84616949bac4a00a9a96d771f6595e7fed371c0a5a54139285311e4c0b367'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/20/GPL/openjdk-24-ea+20_linux-aarch64_bin.tar.gz'; 			downloadSha256='4fe26b4900462d35fcaa9c7b551fd23791906f05eab3a609de8d771cc15ad9d0'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 18 Oct 2024 00:48:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:7d98d813d54f6207a57721008a4081378343ad8f1b2db66c121406019171805b`  
		Last Modified: Thu, 17 Oct 2024 00:23:37 GMT  
		Size: 49.6 MB (49555023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da802df85c965baeca9d39869f9e2cbb3dc844d4627f413bfbb2f2c3d6055988`  
		Last Modified: Sat, 19 Oct 2024 00:54:48 GMT  
		Size: 24.1 MB (24051386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7aadc5092c3b7a865666b14bef3d4d038282b19b124542f1a158c98ea8c1ed1b`  
		Last Modified: Sat, 19 Oct 2024 02:06:37 GMT  
		Size: 64.4 MB (64389695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddc9ead12b54826e53e15bdda2357191fa94d8842198630c6f45ffca0d59b0e5`  
		Last Modified: Sat, 19 Oct 2024 02:54:41 GMT  
		Size: 16.9 MB (16943003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d37cf34ced3af7b701960831d4efce5717f59b8675dda5e69ae29267e55642d8`  
		Last Modified: Sat, 19 Oct 2024 02:54:43 GMT  
		Size: 212.5 MB (212542091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-ea-20-jdk-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:9cb65734659e637115407b93c44d92295de5866e1c2c527b570d0685efff586d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.4 MB (8445653 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a352357a1378fb0857128d31f0b879f74a39c76b612db50a0e45aabd7c2a967`

```dockerfile
```

-	Layers:
	-	`sha256:9f929153286ab614766cc703582ca71302fd24c390f60fb66d6328c2197ee972`  
		Last Modified: Sat, 19 Oct 2024 02:54:41 GMT  
		Size: 8.4 MB (8427035 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d085e453aa664ae98ab75df63ec48dd408288fd75e0f2824d3b4b06425acd74f`  
		Last Modified: Sat, 19 Oct 2024 02:54:40 GMT  
		Size: 18.6 KB (18618 bytes)  
		MIME: application/vnd.in-toto+json
