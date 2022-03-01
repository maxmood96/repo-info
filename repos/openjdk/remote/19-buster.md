## `openjdk:19-buster`

```console
$ docker pull openjdk@sha256:e83c937e4801870053b5f31564508cee9d09220cc0797b01bb7fc7dff459b844
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `openjdk:19-buster` - linux; amd64

```console
$ docker pull openjdk@sha256:33ce98e526dd2476470c1af70cef4a95b6fd2ac6705c9b7fda5e09841032c308
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **324.3 MB (324337467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15eb9a55146caf81c7610fe4ff633034fa12509df376021e78f6620f7a8f26eb`
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
# Tue, 01 Mar 2022 14:21:44 GMT
ENV JAVA_VERSION=19-ea+10
# Tue, 01 Mar 2022 14:21:54 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk19/10/GPL/openjdk-19-ea+10_linux-x64_bin.tar.gz'; 			downloadSha256='21260b7e784c0e74c6730bdbaac70484fde42cf2839b2188dd2c4811d04660d8'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk19/10/GPL/openjdk-19-ea+10_linux-aarch64_bin.tar.gz'; 			downloadSha256='e41beaf49bdb16dc2eeec5e7e7c535f19444e221daf1cbb97d6e2b7981583156'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Tue, 01 Mar 2022 14:21:55 GMT
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
	-	`sha256:605e6fcca705836ac40c154dbb35f17777f1c70de3bd06f0f979b7817ce25786`  
		Last Modified: Tue, 01 Mar 2022 14:42:00 GMT  
		Size: 190.3 MB (190304441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:19-buster` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:94c6f73fe069d6cbcdd9af32b5602adc72dbc11401defca564e70b79546cde95
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **322.9 MB (322875534 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:211081755c0138c4749577b3b9617cf025e746572eb598a979e2a9e3606a0297`
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
# Tue, 01 Mar 2022 13:48:59 GMT
ENV JAVA_VERSION=19-ea+10
# Tue, 01 Mar 2022 13:49:10 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk19/10/GPL/openjdk-19-ea+10_linux-x64_bin.tar.gz'; 			downloadSha256='21260b7e784c0e74c6730bdbaac70484fde42cf2839b2188dd2c4811d04660d8'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk19/10/GPL/openjdk-19-ea+10_linux-aarch64_bin.tar.gz'; 			downloadSha256='e41beaf49bdb16dc2eeec5e7e7c535f19444e221daf1cbb97d6e2b7981583156'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Tue, 01 Mar 2022 13:49:11 GMT
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
	-	`sha256:e3461959adc3f07f7500b31bdfcba421e69fa5fe8696261375edefda14d97761`  
		Last Modified: Tue, 01 Mar 2022 14:14:16 GMT  
		Size: 189.3 MB (189344391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
