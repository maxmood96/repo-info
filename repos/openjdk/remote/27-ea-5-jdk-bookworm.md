## `openjdk:27-ea-5-jdk-bookworm`

```console
$ docker pull openjdk@sha256:d317c190a48d59db82858b947a3fc3f93eb44d9dc2c1ea241a233125acf6a849
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:27-ea-5-jdk-bookworm` - linux; amd64

```console
$ docker pull openjdk@sha256:afadee239f0cc96755e68124594e488940ee99fe1729d28c5460a804f31041a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **382.0 MB (382044823 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8fc0dc01b5254906323f4a348719c21e522013d4f17d0190755ea4bf9206652e`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 02:08:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 03:53:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 20 Jan 2026 18:47:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 20 Jan 2026 18:47:42 GMT
ENV JAVA_HOME=/usr/local/openjdk-27
# Tue, 20 Jan 2026 18:47:42 GMT
ENV PATH=/usr/local/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 20 Jan 2026 18:47:42 GMT
ENV LANG=C.UTF-8
# Tue, 20 Jan 2026 18:47:42 GMT
ENV JAVA_VERSION=27-ea+5
# Tue, 20 Jan 2026 18:47:42 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/5/GPL/openjdk-27-ea+5_linux-x64_bin.tar.gz'; 			downloadSha256='2d85f5a6432abd2eb67b974ed1ab85d2a9557b06be285f2fc6e5d94429951468'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/5/GPL/openjdk-27-ea+5_linux-aarch64_bin.tar.gz'; 			downloadSha256='58f4450fff4f277000cf3d520a612275b0d9b6cb24e1287457d4651e98714b4a'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 20 Jan 2026 18:47:42 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:c1be109a62df95316ceac87ea501079f32e17f36b636865a860841b7db06100c`  
		Last Modified: Tue, 13 Jan 2026 00:41:40 GMT  
		Size: 48.5 MB (48481622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64538a062a61add8dc8b290fa69475e8902eb839c497a5f5dcd5a950422e493c`  
		Last Modified: Tue, 13 Jan 2026 02:09:06 GMT  
		Size: 24.0 MB (24036867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd1872fa12cc6b1145803f1a0679ca26cc65fa1b4e0ee389bfb30267594736b6`  
		Last Modified: Tue, 13 Jan 2026 03:53:27 GMT  
		Size: 64.4 MB (64395833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c51d44a524aa59b5f07253d6add62fb4ded83b2a8abfa419990f5fbc14a9e1a`  
		Last Modified: Tue, 20 Jan 2026 18:48:08 GMT  
		Size: 16.9 MB (16944709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a54468c11d6a9b88e4c96a9175e1fbcc4d193ee960d1b45c488b7f2b651ed95f`  
		Last Modified: Tue, 20 Jan 2026 18:48:12 GMT  
		Size: 228.2 MB (228185792 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-5-jdk-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:bdd1f28d899b258237ed9a8cc86d775827a6a809ea03c533859ac0a50a48dfb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 MB (8686793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d34bdcb71e73b04eb808075d1f4841372ccd00b88f15c47c4bfd267c4742566`

```dockerfile
```

-	Layers:
	-	`sha256:b9a229b6b5441e128e0d77df19c51aaaab9e5cb0394ad5efe136127e3fb78d84`  
		Last Modified: Tue, 20 Jan 2026 18:48:07 GMT  
		Size: 8.7 MB (8668871 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f27737275f2446ed203430172c0dcf876d4a33b486941db23273e594e64e775d`  
		Last Modified: Tue, 20 Jan 2026 19:25:58 GMT  
		Size: 17.9 KB (17922 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:27-ea-5-jdk-bookworm` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:db5437e2626529cd26fd35e9978d6f39dd83bf9bda12a951cd5b8163de3b555f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **380.3 MB (380296356 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6d8e7d1e5ece52ed1d01fd5e42133cbe097a7b807951fdddfb8b267676273b5`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 02:12:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 03:56:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 20 Jan 2026 18:48:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 20 Jan 2026 18:48:23 GMT
ENV JAVA_HOME=/usr/local/openjdk-27
# Tue, 20 Jan 2026 18:48:23 GMT
ENV PATH=/usr/local/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 20 Jan 2026 18:48:23 GMT
ENV LANG=C.UTF-8
# Tue, 20 Jan 2026 18:48:23 GMT
ENV JAVA_VERSION=27-ea+5
# Tue, 20 Jan 2026 18:48:23 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/5/GPL/openjdk-27-ea+5_linux-x64_bin.tar.gz'; 			downloadSha256='2d85f5a6432abd2eb67b974ed1ab85d2a9557b06be285f2fc6e5d94429951468'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/5/GPL/openjdk-27-ea+5_linux-aarch64_bin.tar.gz'; 			downloadSha256='58f4450fff4f277000cf3d520a612275b0d9b6cb24e1287457d4651e98714b4a'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 20 Jan 2026 18:48:23 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1029f5ddc0d24726f1cefbb8def7a88f8ec819a1fdc4c05ce523011b4b73c72d`  
		Last Modified: Tue, 13 Jan 2026 00:41:14 GMT  
		Size: 48.4 MB (48366072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d72c713ab317dd7f302a6ff5a345af5b61cddc864fca2d96a23e6ef3c90a6657`  
		Last Modified: Tue, 13 Jan 2026 02:12:45 GMT  
		Size: 23.6 MB (23604814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:687ad46596f06c934001fa6d7bea3d1508b0bb616cffb71004efd5bada56884f`  
		Last Modified: Tue, 13 Jan 2026 03:57:17 GMT  
		Size: 64.5 MB (64479462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27aa6b4f2d173657bb0a05131c0f60aacf64ab323e19816ad2b4e4b8b66d7390`  
		Last Modified: Tue, 20 Jan 2026 18:48:48 GMT  
		Size: 17.7 MB (17728541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a582491307a3543275dfebdb80ddced74a0c7bad7c96fe2c276ad3c6e1d191b`  
		Last Modified: Tue, 20 Jan 2026 18:57:48 GMT  
		Size: 226.1 MB (226117467 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-5-jdk-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:35a8ce4bb6164636877516f86d7b9db072fcd79609792f6e264d0fdb4bc19468
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8823756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab9639a85520d8f79b8e1ca0c9856e981e8554bfcfe7688dc7d860fc0a2fe09b`

```dockerfile
```

-	Layers:
	-	`sha256:55bb128df96cf8a88dfc5efbe61faf2b64ce03ebfbf730635800099033c01655`  
		Last Modified: Tue, 20 Jan 2026 19:26:06 GMT  
		Size: 8.8 MB (8805716 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bbaa62bbedc66d9373f778af8b6505915ed4e7d0a99f864c111f2f093e908327`  
		Last Modified: Tue, 20 Jan 2026 18:48:47 GMT  
		Size: 18.0 KB (18040 bytes)  
		MIME: application/vnd.in-toto+json
