## `openjdk:26-jdk-bookworm`

```console
$ docker pull openjdk@sha256:195733fc1218f6bfe63d881980145a0b2b734d4460f40d690d4367955347620d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:26-jdk-bookworm` - linux; amd64

```console
$ docker pull openjdk@sha256:b185e52b386db126efdeb8e88d016e29aeb7574bfa4fbff4f8970ec51f22ce50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **377.0 MB (377005710 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f95e6183fa5e610e74ebcb1eae88607dcf454407490a2267b05805c072af8337`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1754870400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 16 Aug 2025 00:56:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 16 Aug 2025 00:56:10 GMT
ENV JAVA_HOME=/usr/local/openjdk-26
# Sat, 16 Aug 2025 00:56:10 GMT
ENV PATH=/usr/local/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 16 Aug 2025 00:56:10 GMT
ENV LANG=C.UTF-8
# Sat, 16 Aug 2025 00:56:10 GMT
ENV JAVA_VERSION=26-ea+11
# Sat, 16 Aug 2025 00:56:10 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/11/GPL/openjdk-26-ea+11_linux-x64_bin.tar.gz'; 			downloadSha256='f37dba6a92e49b69b66df52a6eaadbd068ae8630d3074ca93bd6ebfa8f6e5ad9'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/11/GPL/openjdk-26-ea+11_linux-aarch64_bin.tar.gz'; 			downloadSha256='66798fb794c9b99dd02997b58459ecd7100f79760643ca7fc68cf2303a20b085'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 16 Aug 2025 00:56:10 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f014853ae2033c0e173500a9c5027c3ecffe2ffacbd09b789ac2f2dc63ddaa63`  
		Last Modified: Tue, 12 Aug 2025 20:44:32 GMT  
		Size: 48.5 MB (48494511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d6401b7636bba3fe2d916b154ba44abe2081a737e117b2c736167ca6ea42334`  
		Last Modified: Tue, 12 Aug 2025 22:13:44 GMT  
		Size: 24.0 MB (24020841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cffef7dc6f99e0837fd18f5ab2b363aff8d1c12ed377199f6d6478f80b458c05`  
		Last Modified: Tue, 12 Aug 2025 22:14:50 GMT  
		Size: 64.4 MB (64400050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:970b6c0c0e2ba15fca98ba41010c98e3ce42c23aaf4d1979ec61e82bd1d2ba3a`  
		Last Modified: Mon, 18 Aug 2025 18:16:45 GMT  
		Size: 16.9 MB (16943498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7bc2467196ce2a16f3d12e1a91bee0fa1ba0c3a4d079208d3904cbfc21bc3a9`  
		Last Modified: Mon, 18 Aug 2025 21:37:23 GMT  
		Size: 223.1 MB (223146810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-jdk-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:eaaf8b8da81ef7848070bacc8d04d2914dc2c3a8d14d0e37a8674dc8f4e2df1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 MB (8683184 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:174359ff4bad869ee09db9457c8ad624b4b3628540917157c7a55abbdd28248a`

```dockerfile
```

-	Layers:
	-	`sha256:117b9789e0b293f9419ea764610d1364b411b32aa1e862d639ad9a3840ee95ac`  
		Last Modified: Mon, 18 Aug 2025 21:24:53 GMT  
		Size: 8.7 MB (8664566 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d2306aaa83cb5c1f4ce6a14637f2570305bf4b13ea42225361fdae1a4e36c666`  
		Last Modified: Mon, 18 Aug 2025 21:24:54 GMT  
		Size: 18.6 KB (18618 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:26-jdk-bookworm` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:9b287f8dd8b3252bb82cde5b0724237428122dd610a5f25014ca75b282348548
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **375.0 MB (374991390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00630af14d068e0549232c19a42dbe84a8e37f4513f36ee37f6aed028e9762a0`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1754870400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 16 Aug 2025 00:56:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 16 Aug 2025 00:56:10 GMT
ENV JAVA_HOME=/usr/local/openjdk-26
# Sat, 16 Aug 2025 00:56:10 GMT
ENV PATH=/usr/local/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 16 Aug 2025 00:56:10 GMT
ENV LANG=C.UTF-8
# Sat, 16 Aug 2025 00:56:10 GMT
ENV JAVA_VERSION=26-ea+11
# Sat, 16 Aug 2025 00:56:10 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/11/GPL/openjdk-26-ea+11_linux-x64_bin.tar.gz'; 			downloadSha256='f37dba6a92e49b69b66df52a6eaadbd068ae8630d3074ca93bd6ebfa8f6e5ad9'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/11/GPL/openjdk-26-ea+11_linux-aarch64_bin.tar.gz'; 			downloadSha256='66798fb794c9b99dd02997b58459ecd7100f79760643ca7fc68cf2303a20b085'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 16 Aug 2025 00:56:10 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:35f134665ae4469a16b5b7b841e9efe6b186960e0533131b3603e4816aabeb3a`  
		Last Modified: Tue, 12 Aug 2025 22:08:09 GMT  
		Size: 48.3 MB (48342450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cff9c97e1a1ee42786188e1d1b57f6a2035d65b648178ac0262d0eba0c5c86d`  
		Last Modified: Wed, 13 Aug 2025 07:22:32 GMT  
		Size: 23.6 MB (23569847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4910ed05e8b3022bc1c6adfffae5e35b0d2b4c6d756ee21311b48b509147a1a`  
		Last Modified: Wed, 13 Aug 2025 16:31:39 GMT  
		Size: 64.4 MB (64367003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:224c8c5b8dff524256200adc53415a0d5db5444327a968400e64baa4d5ddfa61`  
		Last Modified: Mon, 18 Aug 2025 22:24:53 GMT  
		Size: 17.7 MB (17727544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28baa4ff12a3159de98cde224c77576dae895fa079aa1b0358dad72495b1127e`  
		Last Modified: Tue, 19 Aug 2025 01:26:54 GMT  
		Size: 221.0 MB (220984546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-jdk-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:eca134f5c62d035358895b9cb97628a0c486bbcc6a20d45fce7c5c1911db1fc6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8820196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aad69508779dc84ffcc3148fa6a351b2516d5b76fd9858aafae045a03033d6cd`

```dockerfile
```

-	Layers:
	-	`sha256:df01972f7693e835b6262fa157dd8fc90a5005eac7e4f2516451f78ec7363a43`  
		Last Modified: Tue, 19 Aug 2025 00:24:37 GMT  
		Size: 8.8 MB (8801435 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1c3dc962973cb7639ba829e0383134e5014267b02f921702cf92194e782440e7`  
		Last Modified: Tue, 19 Aug 2025 00:24:38 GMT  
		Size: 18.8 KB (18761 bytes)  
		MIME: application/vnd.in-toto+json
