## `openjdk:24-rc-bookworm`

```console
$ docker pull openjdk@sha256:09c38805fa2c64627c8394e5b165b2c813f92dfa470916cba3230759fe8a06a7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:24-rc-bookworm` - linux; amd64

```console
$ docker pull openjdk@sha256:e910a7d33bb130249145e5f2cf74f11b3ecc5b3c23f40d5ca83a020706b1cf71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **366.8 MB (366826488 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be44401d974fe9d2702c5527565b8f52c540eaeb35253772821ddf99b61c59bd`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1740355200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 07 Feb 2025 01:48:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 07 Feb 2025 01:48:12 GMT
ENV JAVA_HOME=/usr/local/openjdk-24
# Fri, 07 Feb 2025 01:48:12 GMT
ENV PATH=/usr/local/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 07 Feb 2025 01:48:12 GMT
ENV LANG=C.UTF-8
# Fri, 07 Feb 2025 01:48:12 GMT
ENV JAVA_VERSION=24
# Fri, 07 Feb 2025 01:48:12 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/GA/jdk24/1f9ff9062db4449d8ca828c504ffae90/36/GPL/openjdk-24_linux-x64_bin.tar.gz'; 			downloadSha256='88b090fa80c6c1d084ec9a755233967458788e2c0777ae2e172230c5c692d7ef'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/GA/jdk24/1f9ff9062db4449d8ca828c504ffae90/36/GPL/openjdk-24_linux-aarch64_bin.tar.gz'; 			downloadSha256='a03867ed061c7bb661231e62b0967ff5a5a0b1bbaa37bdead3a924bd2ba3215f'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 07 Feb 2025 01:48:12 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:155ad54a8b2812a0ec559ff82c0c6f0f0dddb337a226b11879f09e15f67b69fc`  
		Last Modified: Tue, 25 Feb 2025 01:29:36 GMT  
		Size: 48.5 MB (48476100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8031108f3cda87bb32f090262d0109c8a0db99168050967becefad502e9a681b`  
		Last Modified: Tue, 25 Feb 2025 02:12:37 GMT  
		Size: 24.1 MB (24058530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d281e50d3e435595c266df06531a7e8c2ebb0c185622c8ab2eed8d760e6576b`  
		Last Modified: Tue, 25 Feb 2025 03:13:36 GMT  
		Size: 64.4 MB (64394215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65fbc23f083e2001dcd437ee300b276c2ba4061e46d56dbfdef6c18cf799a658`  
		Last Modified: Tue, 25 Feb 2025 05:13:36 GMT  
		Size: 16.9 MB (16943053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d3050ecea448436052cc8f213b52910fbd525317ff809ebf1a0e6b32d7ca3a6`  
		Last Modified: Tue, 25 Feb 2025 05:13:39 GMT  
		Size: 213.0 MB (212954590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-rc-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:4b5fa653424e137c47acb60624e1968b52d4f958af3e9771da80067f725e4986
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.5 MB (8457396 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea9dc8dd3b11162511e10ab45ee0cbd6ee5a53958956b78c425c9e0b4e288bf6`

```dockerfile
```

-	Layers:
	-	`sha256:726917764890c5568f8baa00dd2fb58783c841729009ed1fd3d60a46460a0d57`  
		Last Modified: Tue, 25 Feb 2025 05:13:36 GMT  
		Size: 8.4 MB (8439366 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dbf8a7149e6d3b232c19e06448a32a56aed2fbdd0d5111cffe67c6ac12ddd2ec`  
		Last Modified: Tue, 25 Feb 2025 05:13:35 GMT  
		Size: 18.0 KB (18030 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:24-rc-bookworm` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:d29f1c3d8342a274a06adaff69d0d8f0a3a7426bfdd67fd61f0797c6b65c349f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **364.9 MB (364889303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fce5fbdaa9f622975dceafc5ca08d6089de0c9f4c48a3151aa14094c81c1dc87`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1740355200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 07 Feb 2025 01:48:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 07 Feb 2025 01:48:12 GMT
ENV JAVA_HOME=/usr/local/openjdk-24
# Fri, 07 Feb 2025 01:48:12 GMT
ENV PATH=/usr/local/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 07 Feb 2025 01:48:12 GMT
ENV LANG=C.UTF-8
# Fri, 07 Feb 2025 01:48:12 GMT
ENV JAVA_VERSION=24
# Fri, 07 Feb 2025 01:48:12 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/GA/jdk24/1f9ff9062db4449d8ca828c504ffae90/36/GPL/openjdk-24_linux-x64_bin.tar.gz'; 			downloadSha256='88b090fa80c6c1d084ec9a755233967458788e2c0777ae2e172230c5c692d7ef'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/GA/jdk24/1f9ff9062db4449d8ca828c504ffae90/36/GPL/openjdk-24_linux-aarch64_bin.tar.gz'; 			downloadSha256='a03867ed061c7bb661231e62b0967ff5a5a0b1bbaa37bdead3a924bd2ba3215f'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 07 Feb 2025 01:48:12 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:52daf8b0f06f2fdaeb7dec4b92086a6e762488b98364a36c7abb3737d5423d3a`  
		Last Modified: Tue, 25 Feb 2025 01:30:45 GMT  
		Size: 48.3 MB (48308008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5701e2b5d2b168acc741a9ff3fdb127561218f08a68ad5dcc08b3d94a22fc9e`  
		Last Modified: Tue, 25 Feb 2025 05:41:44 GMT  
		Size: 23.6 MB (23598275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31d7468eece796ba37139bc942f068fc99cb7503eb828f59370c3421cca7d528`  
		Last Modified: Tue, 25 Feb 2025 11:54:02 GMT  
		Size: 64.4 MB (64354380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:046da16b58de2e882eaef1b56cc17f316d7db28ddc3122b79fb65a4e2b85f363`  
		Last Modified: Tue, 25 Feb 2025 15:59:30 GMT  
		Size: 17.7 MB (17726670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c417598e8645bbf02be344bd5e255e551c60debbd229359acbfd94a61c670241`  
		Last Modified: Tue, 25 Feb 2025 16:01:44 GMT  
		Size: 210.9 MB (210901970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-rc-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:5ba47b277b35d8b4588a0ee2794daa948e8110039ba84a4e6e65c27a6f192e92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.6 MB (8594359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e17650080ea9b969fb82c0e1aeae8c19b9898e9463c4c4fa2f90cf8483dcdd1`

```dockerfile
```

-	Layers:
	-	`sha256:9d1b8b400082c9e96be32b9fb9c4ed2532a55b81eb7026cd501e76515343b5a7`  
		Last Modified: Tue, 25 Feb 2025 16:01:22 GMT  
		Size: 8.6 MB (8576210 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7c87efd5e896e046830d0f45e578089fbdb15bab9bb8be4f93aa71f0c8c17574`  
		Last Modified: Tue, 25 Feb 2025 16:01:22 GMT  
		Size: 18.1 KB (18149 bytes)  
		MIME: application/vnd.in-toto+json
