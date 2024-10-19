## `openjdk:24-ea-20-bookworm`

```console
$ docker pull openjdk@sha256:6ce8ca1e6b7752ee9a8270ab39d78e8495f14464f9086123f6ec9b1cbb71d578
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:24-ea-20-bookworm` - linux; amd64

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

### `openjdk:24-ea-20-bookworm` - unknown; unknown

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

### `openjdk:24-ea-20-bookworm` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:ffa8a7713d4501a77d63caa8127516b93371445be7709e22deef85e6cb8e01bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **365.7 MB (365677970 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34ba8d353e7f8d6af18b0baff3ef6314d4e9be8bec70d1d9af08cc01763e77b6`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD file:1df819221542e236e104deb2624ffe4efd79382aed25b3ab20088becaeadad31 in / 
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
	-	`sha256:c1e0ef7b956a07c7b090256aa16cbb0550a34d0625d1d23c5b1a76e92a58d01e`  
		Last Modified: Thu, 17 Oct 2024 01:14:19 GMT  
		Size: 49.6 MB (49584978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95b894d63c771a6056bc65ff25192b251413259ba7d160b0076f0f5d7975dc39`  
		Last Modified: Sat, 19 Oct 2024 01:10:43 GMT  
		Size: 23.6 MB (23593834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb5594266b1bacf9ad6855b00d9c5c98e721001eb115218eda673e548e04fdbf`  
		Last Modified: Sat, 19 Oct 2024 05:17:15 GMT  
		Size: 64.4 MB (64350044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b5341981ea72eb0057fdcebfade272f231787fa30c19995eafd8c0976a2846b`  
		Last Modified: Sat, 19 Oct 2024 08:59:50 GMT  
		Size: 17.7 MB (17726616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64fe439b84481cb902adc4bc6b192d915eb7c65bdc68dde5a16120af683b01df`  
		Last Modified: Sat, 19 Oct 2024 08:59:54 GMT  
		Size: 210.4 MB (210422498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-ea-20-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:5a81a1f25f3562f7a55ba1e31e213d8a743f3e33f805374c9ae72e424fc6a0b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.6 MB (8582226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aff0d73c8e2edd46068445f34cba3fa2949b3a6536548a382049c91047206b01`

```dockerfile
```

-	Layers:
	-	`sha256:428a880dfbab41c86d4ac7ffe3f973b6eaa36be7b3e7e9550b47659f26005221`  
		Last Modified: Sat, 19 Oct 2024 08:59:49 GMT  
		Size: 8.6 MB (8563447 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:282d74d5dc042558b4d13c2d769b4822a0450cdb5497ef57dcf4971f48bb9756`  
		Last Modified: Sat, 19 Oct 2024 08:59:49 GMT  
		Size: 18.8 KB (18779 bytes)  
		MIME: application/vnd.in-toto+json
