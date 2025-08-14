## `openjdk:25-jdk-trixie`

```console
$ docker pull openjdk@sha256:e4b550980348fa17e40e713f6777baf38d962135ef08bb2ac446fd9c0d137bdd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:25-jdk-trixie` - linux; amd64

```console
$ docker pull openjdk@sha256:004bf58c9f97c59c536c98ee033b9611dfce66df9773837d3ac636ff0cee4bcf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **381.9 MB (381917479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ea3208a6d7d73ed0e363e19e7445977e3c1342509da0710282beaf8c2bcd789`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1754870400'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 12 Aug 2025 17:48:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 12 Aug 2025 17:48:34 GMT
ENV JAVA_HOME=/usr/local/openjdk-25
# Tue, 12 Aug 2025 17:48:34 GMT
ENV PATH=/usr/local/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Aug 2025 17:48:34 GMT
ENV LANG=C.UTF-8
# Tue, 12 Aug 2025 17:48:34 GMT
ENV JAVA_VERSION=25
# Tue, 12 Aug 2025 17:48:34 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/GA/jdk25/bd75d5f9689641da8e1daabeccb5528b/35/GPL/openjdk-25_linux-x64_bin.tar.gz'; 			downloadSha256='c00224c25b0b915f4d69929d90e59dfd66e949f79f7437d334248f7789b646f4'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/GA/jdk25/bd75d5f9689641da8e1daabeccb5528b/35/GPL/openjdk-25_linux-aarch64_bin.tar.gz'; 			downloadSha256='2cf9e308cd667a6134865652839a3f7d59a93198a10841cb893f65248d1852d7'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 12 Aug 2025 17:48:34 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:80b7316254b3093eb3c7ac44bb6c34bde013f27947c1ed8d8afe456b957ebfdb`  
		Last Modified: Tue, 12 Aug 2025 20:45:14 GMT  
		Size: 49.3 MB (49278280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36e4db86de6eba33869491caa7946b80dd71c255f1940e96a9f755cc2b1f3829`  
		Last Modified: Tue, 12 Aug 2025 22:14:12 GMT  
		Size: 25.6 MB (25612940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ea45766c6449310ca2fc621a7e00bedb4b9b803a7fbfe2607efce6d2e07e435`  
		Last Modified: Tue, 12 Aug 2025 22:15:03 GMT  
		Size: 67.8 MB (67777316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fdb2712779fc5fdd0a9ee46101620d73b507066a8b99132315713364e6bcd61`  
		Last Modified: Tue, 12 Aug 2025 23:39:45 GMT  
		Size: 16.1 MB (16061242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe98fa01b937960775e55b24a1324e88427e0b665e7f25ea3537af4ea407f46d`  
		Last Modified: Wed, 13 Aug 2025 00:39:37 GMT  
		Size: 223.2 MB (223187701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-jdk-trixie` - unknown; unknown

```console
$ docker pull openjdk@sha256:b8e2138887247899794c6ea3017526c062732b79579d2b874f7936a62ce7f6f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.5 MB (8526326 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36ab3999ed65df5a30024ff6cdd83ee382056276f7c53f6dd728adaa62850f3e`

```dockerfile
```

-	Layers:
	-	`sha256:871ea922f953a91c9db6a7223ab1160d31613d5581c336a39c3dbf1585b6aad1`  
		Last Modified: Wed, 13 Aug 2025 00:23:51 GMT  
		Size: 8.5 MB (8508322 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:70128d5dd7126191bbcbf3cbd827e4a11edf29778f36044e63af06d8a91b2f24`  
		Last Modified: Wed, 13 Aug 2025 00:23:52 GMT  
		Size: 18.0 KB (18004 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:25-jdk-trixie` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:ffcd009ecbd0114d6936a61cbac1eba819b63037bc1f874cc18f9449f9be7ae3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **379.3 MB (379303991 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65ebb9ee11deeffc68579f7792141265d9d77438cbdb15e35854c6518903efe9`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1754870400'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 12 Aug 2025 17:48:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 12 Aug 2025 17:48:34 GMT
ENV JAVA_HOME=/usr/local/openjdk-25
# Tue, 12 Aug 2025 17:48:34 GMT
ENV PATH=/usr/local/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Aug 2025 17:48:34 GMT
ENV LANG=C.UTF-8
# Tue, 12 Aug 2025 17:48:34 GMT
ENV JAVA_VERSION=25
# Tue, 12 Aug 2025 17:48:34 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/GA/jdk25/bd75d5f9689641da8e1daabeccb5528b/35/GPL/openjdk-25_linux-x64_bin.tar.gz'; 			downloadSha256='c00224c25b0b915f4d69929d90e59dfd66e949f79f7437d334248f7789b646f4'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/GA/jdk25/bd75d5f9689641da8e1daabeccb5528b/35/GPL/openjdk-25_linux-aarch64_bin.tar.gz'; 			downloadSha256='2cf9e308cd667a6134865652839a3f7d59a93198a10841cb893f65248d1852d7'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 12 Aug 2025 17:48:34 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:d1e40442030765a3ac5d135c39154d052eba20953ea0e5d35a066f7722cdd93d`  
		Last Modified: Tue, 12 Aug 2025 22:12:36 GMT  
		Size: 49.6 MB (49641603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9923852056eb09462c3344515191318e7aa33ff28057c946bc41a414ee57df0b`  
		Last Modified: Wed, 13 Aug 2025 07:30:07 GMT  
		Size: 25.0 MB (25014610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bcc8bff74cbeacbac9c6869b6a9def273b93cc67de196b347688de2a9185de0`  
		Last Modified: Wed, 13 Aug 2025 15:31:50 GMT  
		Size: 67.6 MB (67593628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7bec944219f19e96419bed7e049266968a53d429d56885b248ff9a63b06a4d4`  
		Last Modified: Wed, 13 Aug 2025 22:27:43 GMT  
		Size: 16.1 MB (16070219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4b28c8bd8554b4ed5451664623297b3435edf9795968abd230fbbc31df68d3b`  
		Last Modified: Thu, 14 Aug 2025 21:45:56 GMT  
		Size: 221.0 MB (220983931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-jdk-trixie` - unknown; unknown

```console
$ docker pull openjdk@sha256:50558a7c07ad456a3d5480259b14381c889ce38ff2f82bb0d2605152dcf34e35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 MB (8721235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed9833cfc01f75058827163274a89bc88e8f1da863fb337973978ab20c508333`

```dockerfile
```

-	Layers:
	-	`sha256:75862ebc71249ad03993feefc176b265d274babc31825fe8092f06aaa1ba20b2`  
		Last Modified: Thu, 14 Aug 2025 00:23:35 GMT  
		Size: 8.7 MB (8703112 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6196fd3a225d559bddd05c82246cf44d85699767ee0a48d3c02722768cbfdad3`  
		Last Modified: Thu, 14 Aug 2025 00:23:36 GMT  
		Size: 18.1 KB (18123 bytes)  
		MIME: application/vnd.in-toto+json
