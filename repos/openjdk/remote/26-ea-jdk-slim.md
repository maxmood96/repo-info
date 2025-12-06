## `openjdk:26-ea-jdk-slim`

```console
$ docker pull openjdk@sha256:482be01596826d3bab455fa1d64d47babfb76f0f5a58e7e83814776f89576028
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:26-ea-jdk-slim` - linux; amd64

```console
$ docker pull openjdk@sha256:8e933a89c829d8dda01d78c91e9a18d5467585009cbd64957744e202875b5d4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **260.1 MB (260132232 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1aca7418d155eb854b14ecc486dc7c0b70e8133fd8a1cc0c03b28bad44322904`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1763337600'
# Sat, 06 Dec 2025 00:34:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 06 Dec 2025 00:34:42 GMT
ENV JAVA_HOME=/usr/local/openjdk-26
# Sat, 06 Dec 2025 00:34:42 GMT
ENV PATH=/usr/local/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 06 Dec 2025 00:34:42 GMT
ENV LANG=C.UTF-8
# Sat, 06 Dec 2025 00:34:42 GMT
ENV JAVA_VERSION=26-ea+27
# Sat, 06 Dec 2025 00:34:42 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/27/GPL/openjdk-26-ea+27_linux-x64_bin.tar.gz'; 			downloadSha256='c219dd04012af56a87523d69c6dd07a66adce846ff11981335a361ae9e0b4472'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/27/GPL/openjdk-26-ea+27_linux-aarch64_bin.tar.gz'; 			downloadSha256='8b59cc8266e8d1eadc2919567b907da7098542b2c0d602eb73484728a0e7b2f7'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 06 Dec 2025 00:34:42 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:0e4bc2bd6656e6e004e3c749af70e5650bac2258243eb0949dea51cb8b7863db`  
		Last Modified: Tue, 18 Nov 2025 02:35:01 GMT  
		Size: 29.8 MB (29776484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0cc1e9302cae4082d8b59544abbd9fb2ec068ef1b2a0c9150f96f3d944ae6e3`  
		Last Modified: Sat, 06 Dec 2025 00:35:16 GMT  
		Size: 2.4 MB (2371016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfec652ab03329511606c0013d4c515526518a6c6aeccf559ff2e2143dfc9b85`  
		Last Modified: Sat, 06 Dec 2025 00:35:23 GMT  
		Size: 228.0 MB (227984732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-ea-jdk-slim` - unknown; unknown

```console
$ docker pull openjdk@sha256:3dd07624451224c4926f5c5bbba75559573bd52e4fab3f438c69cfbbd3fcc32a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2296898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33d0d70e4242307f7e19f115380cbf929603515f59ee4a7715359226ed5da209`

```dockerfile
```

-	Layers:
	-	`sha256:596446fd4887a6fbb453f805f51391e080ca629d154436b593b8d2f6c66c65e2`  
		Last Modified: Sat, 06 Dec 2025 01:24:11 GMT  
		Size: 2.3 MB (2278789 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:78104c44c6fd837241120798b02bdd058c805d29ec28d261fd5df4de26d87fbc`  
		Last Modified: Sat, 06 Dec 2025 01:24:12 GMT  
		Size: 18.1 KB (18109 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:26-ea-jdk-slim` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:15a14cc7c973db73e8742958000b50f49a339d429b16046296170c12e0515ef1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.4 MB (258356977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bcff3cc22c6555a50876049c13b37f2ce069d0d5aba8afb50fb3980d3832753`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1763337600'
# Sat, 06 Dec 2025 00:34:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 06 Dec 2025 00:35:07 GMT
ENV JAVA_HOME=/usr/local/openjdk-26
# Sat, 06 Dec 2025 00:35:07 GMT
ENV PATH=/usr/local/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 06 Dec 2025 00:35:07 GMT
ENV LANG=C.UTF-8
# Sat, 06 Dec 2025 00:35:07 GMT
ENV JAVA_VERSION=26-ea+27
# Sat, 06 Dec 2025 00:35:07 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/27/GPL/openjdk-26-ea+27_linux-x64_bin.tar.gz'; 			downloadSha256='c219dd04012af56a87523d69c6dd07a66adce846ff11981335a361ae9e0b4472'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/27/GPL/openjdk-26-ea+27_linux-aarch64_bin.tar.gz'; 			downloadSha256='8b59cc8266e8d1eadc2919567b907da7098542b2c0d602eb73484728a0e7b2f7'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 06 Dec 2025 00:35:07 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:b89cf3ec7a3ed3a58015edd6724125187f0d284147e09b5739b511c74222b2a4`  
		Last Modified: Tue, 18 Nov 2025 01:13:26 GMT  
		Size: 30.1 MB (30138610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:161e2caa0e0ecbeab55ac3f17d8b79eeee8d1e77eb16bd3a7928f5a3ade29452`  
		Last Modified: Sat, 06 Dec 2025 00:35:41 GMT  
		Size: 2.3 MB (2314072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:005fa8e19e505cc4ad94022be5135ebd2c8e01825ba4f38003afa57397d7c33a`  
		Last Modified: Sat, 06 Dec 2025 00:35:54 GMT  
		Size: 225.9 MB (225904295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-ea-jdk-slim` - unknown; unknown

```console
$ docker pull openjdk@sha256:30093a739570eb1265e7b9972d35da62f5c8880d8496139de3456c37a788f7dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2296750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86f97e3c3de890185dfd69e57a4176808fbb0c8afd84343f41243f4067dc8ac1`

```dockerfile
```

-	Layers:
	-	`sha256:b76be8853f70ac8c73b936ff59705a5c97054040045a20ad89dca0952fe1913d`  
		Last Modified: Sat, 06 Dec 2025 01:24:15 GMT  
		Size: 2.3 MB (2278475 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d7f01077b06dfb5ad40fbcaaa25128d1a154f640ac80cef3676e6c1724c26cff`  
		Last Modified: Sat, 06 Dec 2025 01:24:16 GMT  
		Size: 18.3 KB (18275 bytes)  
		MIME: application/vnd.in-toto+json
