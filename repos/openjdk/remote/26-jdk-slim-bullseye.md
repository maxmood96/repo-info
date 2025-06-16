## `openjdk:26-jdk-slim-bullseye`

```console
$ docker pull openjdk@sha256:863e0d6478f1ca545cbcdda1447e32560f84e107cefae68be901cecb7df4ea39
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:26-jdk-slim-bullseye` - linux; amd64

```console
$ docker pull openjdk@sha256:68751905f23556b163029fa396d8d99525f9eb795c3d826754ce83993e1560da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **254.8 MB (254774060 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cde9eeb8a956de10db3d874237f06ebc4034e4836f1f77f7c5ab7d89e691284d`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 10 Jun 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1749513600'
# Sat, 14 Jun 2025 00:54:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 14 Jun 2025 00:54:06 GMT
ENV JAVA_HOME=/usr/local/openjdk-26
# Sat, 14 Jun 2025 00:54:06 GMT
ENV PATH=/usr/local/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 14 Jun 2025 00:54:06 GMT
ENV LANG=C.UTF-8
# Sat, 14 Jun 2025 00:54:06 GMT
ENV JAVA_VERSION=26-ea+2
# Sat, 14 Jun 2025 00:54:06 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/2/GPL/openjdk-26-ea+2_linux-x64_bin.tar.gz'; 			downloadSha256='433a629dd1072b3147cce33cf79ae06ba8c7aa9aac53f403330e8f10ec12ca76'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/2/GPL/openjdk-26-ea+2_linux-aarch64_bin.tar.gz'; 			downloadSha256='5f413ff4f8e92fcdeaf0da5315a51d2165a4017852a4a6c7e2731a8aae19e2e7'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 14 Jun 2025 00:54:06 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3d79ccbe0210f4986821cddffc5c7fc6551d938e282044db7571e448bde1e24a`  
		Last Modified: Tue, 10 Jun 2025 23:27:03 GMT  
		Size: 30.3 MB (30256064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97e6c767aa146f7453aa7d3bbe88129e98e29bc2f5d882ca66e74597f5789343`  
		Last Modified: Mon, 16 Jun 2025 17:50:59 GMT  
		Size: 1.6 MB (1583569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a749578f533b902596c385644689297017c3acc1d4b85eda9c5b703be3ad246c`  
		Last Modified: Mon, 16 Jun 2025 18:52:32 GMT  
		Size: 222.9 MB (222934427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-jdk-slim-bullseye` - unknown; unknown

```console
$ docker pull openjdk@sha256:43e755f757a60dccd2c891015fd4107f19afd6348a441c1b6ade243128d33655
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2960197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4b246ff1f19c9736a0253f35128c1b7ff1c3db5585ea89250868463dc84ae4c`

```dockerfile
```

-	Layers:
	-	`sha256:9770e27f9144af6096e8e566a9ecac44adf9d58549fd04de318ce7f9f084425c`  
		Last Modified: Mon, 16 Jun 2025 18:25:57 GMT  
		Size: 2.9 MB (2942640 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4516b290139af19dde5d4f3a6e714ad5bfdc4426b4d4a08cba6b331e2d5a9a66`  
		Last Modified: Mon, 16 Jun 2025 18:25:57 GMT  
		Size: 17.6 KB (17557 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:26-jdk-slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:0013b4898e6c5b61c98badff5815c4c137b916ea21d2d9f74c85b186f8477301
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **251.0 MB (251047730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:229dce3dc95464a980f41c22d4918d4ca8584e3e5a394b708a1966cd29ed1e25`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 10 Jun 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1749513600'
# Sat, 14 Jun 2025 00:54:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 14 Jun 2025 00:54:06 GMT
ENV JAVA_HOME=/usr/local/openjdk-26
# Sat, 14 Jun 2025 00:54:06 GMT
ENV PATH=/usr/local/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 14 Jun 2025 00:54:06 GMT
ENV LANG=C.UTF-8
# Sat, 14 Jun 2025 00:54:06 GMT
ENV JAVA_VERSION=26-ea+2
# Sat, 14 Jun 2025 00:54:06 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/2/GPL/openjdk-26-ea+2_linux-x64_bin.tar.gz'; 			downloadSha256='433a629dd1072b3147cce33cf79ae06ba8c7aa9aac53f403330e8f10ec12ca76'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/2/GPL/openjdk-26-ea+2_linux-aarch64_bin.tar.gz'; 			downloadSha256='5f413ff4f8e92fcdeaf0da5315a51d2165a4017852a4a6c7e2731a8aae19e2e7'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 14 Jun 2025 00:54:06 GMT
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
	-	`sha256:d79085c3f63d3bef958f36d85f630d633defef712e8aa94fae637f3cd6d154cf`  
		Last Modified: Mon, 16 Jun 2025 18:52:32 GMT  
		Size: 220.7 MB (220736336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-jdk-slim-bullseye` - unknown; unknown

```console
$ docker pull openjdk@sha256:9866709059eba197577d78446d289ffd72630347195d2041d241301bd3510d9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2959992 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6cd78a78cf6365a5536a55713732325a48ce0499d18ec1072495d084747def15`

```dockerfile
```

-	Layers:
	-	`sha256:fb58c419f73fe2316a0465f9de5bda736f44c731d7953fb24c80413ba184339c`  
		Last Modified: Mon, 16 Jun 2025 18:26:02 GMT  
		Size: 2.9 MB (2942292 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d6101f36a27775cf662d51fe3f29ad340cdbba0b22c54aa26bfa69aec1b47273`  
		Last Modified: Mon, 16 Jun 2025 18:26:03 GMT  
		Size: 17.7 KB (17700 bytes)  
		MIME: application/vnd.in-toto+json
