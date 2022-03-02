## `openjdk:19-jdk-buster`

```console
$ docker pull openjdk@sha256:36dd1154e5ef696817040d34727610d913e8550d066e4d82ffca73de41633fc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `openjdk:19-jdk-buster` - linux; amd64

```console
$ docker pull openjdk@sha256:273f348543573f51ad4dbe7384d5e6d28613e10555af3500f2186325a8116b32
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **327.1 MB (327145447 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a80f5e8ce6f35fd5a3eab63b7670348f51199e67f0b577c29817ea7db134845c`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 01 Mar 2022 02:13:41 GMT
ADD file:e8b516b464e535b435a6ed8609bac98acc90ee30e2a0667f68932f0d924f6e49 in / 
# Tue, 01 Mar 2022 02:13:42 GMT
CMD ["bash"]
# Tue, 01 Mar 2022 06:27:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 06:28:02 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 01 Mar 2022 06:28:26 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 14:21:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 14:21:44 GMT
ENV JAVA_HOME=/usr/local/openjdk-19
# Tue, 01 Mar 2022 14:21:44 GMT
ENV PATH=/usr/local/openjdk-19/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Mar 2022 14:21:44 GMT
ENV LANG=C.UTF-8
# Wed, 02 Mar 2022 19:58:08 GMT
ENV JAVA_VERSION=19-ea+11
# Wed, 02 Mar 2022 19:58:18 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk19/11/GPL/openjdk-19-ea+11_linux-x64_bin.tar.gz'; 			downloadSha256='df51ead7190d118175654b6d0688649e67ffe6f23e84d30584145ce3908281e1'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk19/11/GPL/openjdk-19-ea+11_linux-aarch64_bin.tar.gz'; 			downloadSha256='4edb9b2995bb4727d03834c22b36adc9d90b3e75a173420474bad629853756d4'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Wed, 02 Mar 2022 19:58:19 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1c9a8b42b5780ac49c71f392c9512c0167ecc23de9b30b1b5f38747b73097d1a`  
		Last Modified: Tue, 01 Mar 2022 02:19:43 GMT  
		Size: 50.4 MB (50437046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:163066942b43a00ba7f4674c4c1ca90eccc8d99366a3dc47cb64e06ad79c36e5`  
		Last Modified: Tue, 01 Mar 2022 06:37:36 GMT  
		Size: 7.8 MB (7834052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf70e03a8272d87e65c7b1592f97f6e739cf1f5d13cc536670f41c28b086b4cb`  
		Last Modified: Tue, 01 Mar 2022 06:37:37 GMT  
		Size: 10.0 MB (9997298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86c5ff33549498a7154441116b5843e184c1f4441df2eab519ad2c498cb8a716`  
		Last Modified: Tue, 01 Mar 2022 06:37:56 GMT  
		Size: 51.8 MB (51843267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57a64246d99aee8722efa51b8b2198000564a73d3ce50f9d765d22caa7f6ee1c`  
		Last Modified: Tue, 01 Mar 2022 14:41:42 GMT  
		Size: 13.9 MB (13921363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:503218cfa1d0edc8ba6ede7bf8d7d279667ba70af759bbb66a27eaf814b364c4`  
		Last Modified: Wed, 02 Mar 2022 20:09:53 GMT  
		Size: 193.1 MB (193112421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:19-jdk-buster` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:b12dfa8dd91eeaa4477ce4a677d74cb469ea41652113bcffc82d66496ebb0374
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **325.7 MB (325672901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6dd25151db3cf4f8d21dd9c11e42eedcce26149bd225c884ef0431e26befe8e0`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 01 Mar 2022 02:11:41 GMT
ADD file:ec3d90624857dbfae217c1372a38966f453fcd51282379652f07d2ccf6fcc67e in / 
# Tue, 01 Mar 2022 02:11:42 GMT
CMD ["bash"]
# Tue, 01 Mar 2022 10:35:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 10:35:21 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 01 Mar 2022 10:35:43 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 13:48:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 13:48:56 GMT
ENV JAVA_HOME=/usr/local/openjdk-19
# Tue, 01 Mar 2022 13:48:57 GMT
ENV PATH=/usr/local/openjdk-19/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Mar 2022 13:48:58 GMT
ENV LANG=C.UTF-8
# Wed, 02 Mar 2022 08:05:58 GMT
ENV JAVA_VERSION=19-ea+11
# Wed, 02 Mar 2022 08:06:19 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk19/11/GPL/openjdk-19-ea+11_linux-x64_bin.tar.gz'; 			downloadSha256='df51ead7190d118175654b6d0688649e67ffe6f23e84d30584145ce3908281e1'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk19/11/GPL/openjdk-19-ea+11_linux-aarch64_bin.tar.gz'; 			downloadSha256='4edb9b2995bb4727d03834c22b36adc9d90b3e75a173420474bad629853756d4'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Wed, 02 Mar 2022 08:06:20 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:72f0eb753e825356fa0fef854ac259cc8eefdb0f689516f29b13da8b1595c342`  
		Last Modified: Tue, 01 Mar 2022 02:18:46 GMT  
		Size: 49.2 MB (49223022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93053a54416be8288cbcc300d0a929f1279cceff9eb11ad9c080fe5439d62dbd`  
		Last Modified: Tue, 01 Mar 2022 10:45:39 GMT  
		Size: 7.7 MB (7695236 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2387f0e2dcc6f4271b34d3158d1768015e4424839f06ae428f4e22de8a5c1542`  
		Last Modified: Tue, 01 Mar 2022 10:45:40 GMT  
		Size: 9.8 MB (9767253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08d8752c30aea58b7ac6dd29ed3dee03ac8ecb3aedcc6e23ba5ddaac39d89f0b`  
		Last Modified: Tue, 01 Mar 2022 10:45:58 GMT  
		Size: 52.2 MB (52174602 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11179061655cbc71dfb8c2d9d6954e03aa8a708c9a8ff9b742ae15384aae5e3c`  
		Last Modified: Tue, 01 Mar 2022 14:14:02 GMT  
		Size: 14.7 MB (14671030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d5afbf49db536a06cf178c53b7a947f95ace45efe0c544fac528bc69d13140a`  
		Last Modified: Wed, 02 Mar 2022 08:21:32 GMT  
		Size: 192.1 MB (192141758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
