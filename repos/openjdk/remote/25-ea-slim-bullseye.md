## `openjdk:25-ea-slim-bullseye`

```console
$ docker pull openjdk@sha256:0ab71394b3c8833b3cfff6dc901c990933d332886563f65fdef8640998801c82
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:25-ea-slim-bullseye` - linux; amd64

```console
$ docker pull openjdk@sha256:9ecb98883e9d35c10e58f2dfe1ef62938e795209d5e4e419a063cf3e7051fbfc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.0 MB (254976894 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82a4d5ff2fdd3d16f21987cd1207ba97f680e259ec4efb47a00939b16c5ea0e8`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 10 Jun 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1749513600'
# Sat, 14 Jun 2025 00:48:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 14 Jun 2025 00:48:10 GMT
ENV JAVA_HOME=/usr/local/openjdk-25
# Sat, 14 Jun 2025 00:48:10 GMT
ENV PATH=/usr/local/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 14 Jun 2025 00:48:10 GMT
ENV LANG=C.UTF-8
# Sat, 14 Jun 2025 00:48:10 GMT
ENV JAVA_VERSION=25-ea+27
# Sat, 14 Jun 2025 00:48:10 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/27/GPL/openjdk-25-ea+27_linux-x64_bin.tar.gz'; 			downloadSha256='96753b911566d9a6bcbdc84cde764dad6ac5250976260bbd3af509765ddfc8bf'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/27/GPL/openjdk-25-ea+27_linux-aarch64_bin.tar.gz'; 			downloadSha256='d4dee2002500348945826f4377fe2b480b57fc39fe5ac9cefe09ee46f36fd2d3'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 14 Jun 2025 00:48:10 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3d79ccbe0210f4986821cddffc5c7fc6551d938e282044db7571e448bde1e24a`  
		Last Modified: Tue, 10 Jun 2025 23:27:03 GMT  
		Size: 30.3 MB (30256064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d68dea384c594f3346e7dbe4d58cf2998698afcff40086cf7f52902e14adf624`  
		Last Modified: Mon, 16 Jun 2025 17:51:16 GMT  
		Size: 1.6 MB (1583575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5899071de8d3fe682c4b602ef443807c61c15695032c7aa4b79e25f3b40a22bd`  
		Last Modified: Mon, 16 Jun 2025 18:33:01 GMT  
		Size: 223.1 MB (223137255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-ea-slim-bullseye` - unknown; unknown

```console
$ docker pull openjdk@sha256:9231a7848e166209b213d4376e1c80ae64fbd6af3e830a9c11a86613c87ea75b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2960219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17e6d605ab69da078e3a50a0e540854c227b9e706a2a7d3b549c83f6f4e4c94f`

```dockerfile
```

-	Layers:
	-	`sha256:913df73d1af5a3b59b1ca9f0c602152847f6adbed6cee2fa9c4742ce3fe4a3cb`  
		Last Modified: Mon, 16 Jun 2025 18:24:10 GMT  
		Size: 2.9 MB (2942650 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c8660a0b963e46d92d7a6aaa12769209e72e573eba5846576bb0463fb1d3bbda`  
		Last Modified: Mon, 16 Jun 2025 18:24:11 GMT  
		Size: 17.6 KB (17569 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:25-ea-slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:e7f14018f91a3c33a62b8ababce6cee104f7ead4b27eb4f31dbc902b04162dd0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **251.2 MB (251244972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ac742c7bc971556b89d3a9ce992f12a8f5e2a5bac7ec05237c85429987f5a47`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 10 Jun 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1749513600'
# Sat, 14 Jun 2025 00:48:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 14 Jun 2025 00:48:10 GMT
ENV JAVA_HOME=/usr/local/openjdk-25
# Sat, 14 Jun 2025 00:48:10 GMT
ENV PATH=/usr/local/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 14 Jun 2025 00:48:10 GMT
ENV LANG=C.UTF-8
# Sat, 14 Jun 2025 00:48:10 GMT
ENV JAVA_VERSION=25-ea+27
# Sat, 14 Jun 2025 00:48:10 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/27/GPL/openjdk-25-ea+27_linux-x64_bin.tar.gz'; 			downloadSha256='96753b911566d9a6bcbdc84cde764dad6ac5250976260bbd3af509765ddfc8bf'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/27/GPL/openjdk-25-ea+27_linux-aarch64_bin.tar.gz'; 			downloadSha256='d4dee2002500348945826f4377fe2b480b57fc39fe5ac9cefe09ee46f36fd2d3'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 14 Jun 2025 00:48:10 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1efb2a16e6255fa81193190b623ba0668ffa777ab1de41ac5c5d2d2060a47784`  
		Last Modified: Wed, 11 Jun 2025 00:07:31 GMT  
		Size: 28.7 MB (28744185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91c2d2b95084a3992142933bdd33c152ff4bcd950f847b08cb85dfead42aa714`  
		Last Modified: Mon, 16 Jun 2025 17:55:14 GMT  
		Size: 1.6 MB (1567209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c773aa03f9bb3857778d75f4bc19d69b6b50ea29f784cbbaa0a9659a3b498d91`  
		Last Modified: Mon, 16 Jun 2025 18:33:22 GMT  
		Size: 220.9 MB (220933578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-ea-slim-bullseye` - unknown; unknown

```console
$ docker pull openjdk@sha256:6ec67f8d38708d065f729c0f06530eadefe039f2cbf21f5db96db191bbdd0893
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2960014 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c66692da7e7aaab85ed82b91d04dd56150f4cc2682f9b23a08718f2f5084e93`

```dockerfile
```

-	Layers:
	-	`sha256:6f025fe7b287ec17764dcefc7e0b7a0e49bcb3cb1df3dc3d8f4d7ea818391046`  
		Last Modified: Mon, 16 Jun 2025 18:24:15 GMT  
		Size: 2.9 MB (2942302 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b93f2d5d8697502da5559d0da6b34b30f74bb19ac4da6cde12a49660b3c85b7f`  
		Last Modified: Mon, 16 Jun 2025 18:24:16 GMT  
		Size: 17.7 KB (17712 bytes)  
		MIME: application/vnd.in-toto+json
