## `openjdk:27-ea-11-slim-bookworm`

```console
$ docker pull openjdk@sha256:ca4063af364c08f18c1c5ea5d190b69517e454b6fc89422c1a8b5d615e836231
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:27-ea-11-slim-bookworm` - linux; amd64

```console
$ docker pull openjdk@sha256:d350c067dced3aa2e4f719274fe0580d1453801772f75fb17b302cbbd3c030fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **260.9 MB (260851558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34cbcc2ec54d965633de5038e3bd2229a67009b52f110ae0869ad56a73ecda6b`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1771804800'
# Mon, 02 Mar 2026 21:25:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 02 Mar 2026 21:25:40 GMT
ENV JAVA_HOME=/usr/local/openjdk-27
# Mon, 02 Mar 2026 21:25:40 GMT
ENV PATH=/usr/local/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Mar 2026 21:25:40 GMT
ENV LANG=C.UTF-8
# Mon, 02 Mar 2026 21:25:40 GMT
ENV JAVA_VERSION=27-ea+11
# Mon, 02 Mar 2026 21:25:40 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/11/GPL/openjdk-27-ea+11_linux-x64_bin.tar.gz'; 			downloadSha256='75a300b52539589c8c4b172ef292d5b58486de4d88d774be659975bc661767bf'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/11/GPL/openjdk-27-ea+11_linux-aarch64_bin.tar.gz'; 			downloadSha256='3bf27bc49545e677311a0eab8a838953f4726191499accef492c7feaf801e429'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Mon, 02 Mar 2026 21:25:40 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:84a2afebaf4de2e8eb885634a69abd0087b79c947c53fa4f0481235d6dfadc6c`  
		Last Modified: Tue, 24 Feb 2026 18:43:00 GMT  
		Size: 28.2 MB (28236279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8c4bc56a27c9852ff395f9d35eb988dad0d58e000eb3dfc7d1fe1f05b7101aa`  
		Last Modified: Mon, 02 Mar 2026 21:25:59 GMT  
		Size: 4.0 MB (4029192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69dbd085cdf78a38926415cdcfaced25cb318f0dae2b9a09d940deb6470ccc3c`  
		Last Modified: Mon, 02 Mar 2026 21:26:04 GMT  
		Size: 228.6 MB (228586087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-11-slim-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:fcc1d591233e32bea31b743760b56cc12fa0ca7ae5491d1b43a286f81540ebd3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2666676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be750efd3df7ab957a3ab6e27c8a9b0ce250838531831472e43692ed0200c90f`

```dockerfile
```

-	Layers:
	-	`sha256:fce6d01c4de906b8e0287043623b6085f3ddd6fb97a8d7d61036ca09604fe8d0`  
		Last Modified: Mon, 02 Mar 2026 21:25:59 GMT  
		Size: 2.6 MB (2649805 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:219847c33e344c2634b79a372bb5f14114319665f61c17375e3e34d92a14afa4`  
		Last Modified: Mon, 02 Mar 2026 21:25:59 GMT  
		Size: 16.9 KB (16871 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:27-ea-11-slim-bookworm` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:8e40c05357fc43bd11d1bef56f397122299036e61e546ca8b75758c026c5a053
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.5 MB (258498609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fea2969eab17f580b0b2dc38fbbcdb055d2abe7ec64e2a48c53b668fa7cc3706`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1771804800'
# Mon, 02 Mar 2026 21:25:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 02 Mar 2026 21:25:39 GMT
ENV JAVA_HOME=/usr/local/openjdk-27
# Mon, 02 Mar 2026 21:25:39 GMT
ENV PATH=/usr/local/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Mar 2026 21:25:39 GMT
ENV LANG=C.UTF-8
# Mon, 02 Mar 2026 21:25:39 GMT
ENV JAVA_VERSION=27-ea+11
# Mon, 02 Mar 2026 21:25:39 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/11/GPL/openjdk-27-ea+11_linux-x64_bin.tar.gz'; 			downloadSha256='75a300b52539589c8c4b172ef292d5b58486de4d88d774be659975bc661767bf'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/11/GPL/openjdk-27-ea+11_linux-aarch64_bin.tar.gz'; 			downloadSha256='3bf27bc49545e677311a0eab8a838953f4726191499accef492c7feaf801e429'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Mon, 02 Mar 2026 21:25:39 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:eb04ef52de3a23999fcda632f100324a4d1dbebd588b4df190c4a172bb88c603`  
		Last Modified: Tue, 24 Feb 2026 18:42:16 GMT  
		Size: 28.1 MB (28116081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c6536abe633bb6567e2748b55856cc4897b894a4246cfd08a10a95ca9b5195c`  
		Last Modified: Mon, 02 Mar 2026 21:26:00 GMT  
		Size: 3.9 MB (3851966 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cbbd2f940b7a0092d6a0b899d00032c8a7e70a73515e8223a581a975eb6084e`  
		Last Modified: Mon, 02 Mar 2026 21:26:07 GMT  
		Size: 226.5 MB (226530562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-11-slim-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:4df814f3e71dad400c5deb1700e9169a01f3ef51f3f3e93c8bc314c8eaae9ae2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2666429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eed1fa2c89915e2f1606befe821199c21d6ba3368e70978917339ab6a37743b3`

```dockerfile
```

-	Layers:
	-	`sha256:c8bd3e85122c7ca3666b62607b558ccac24c25e8dcfeefe9588b1e6967630135`  
		Last Modified: Mon, 02 Mar 2026 21:26:00 GMT  
		Size: 2.6 MB (2649439 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fed9532928209bbf3006f39b80b07593bdeeb73e757d18531ecc7b9a84078a1a`  
		Last Modified: Mon, 02 Mar 2026 21:26:00 GMT  
		Size: 17.0 KB (16990 bytes)  
		MIME: application/vnd.in-toto+json
