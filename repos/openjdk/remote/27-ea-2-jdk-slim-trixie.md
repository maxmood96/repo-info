## `openjdk:27-ea-2-jdk-slim-trixie`

```console
$ docker pull openjdk@sha256:38c8e216156c201bdc1719714be93610b0261fc26358842e985c9695f5244377
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:27-ea-2-jdk-slim-trixie` - linux; amd64

```console
$ docker pull openjdk@sha256:b4dd987c6b3c30af54dc7dc194e78cd12729d3e17b9f5ed6e857625d6975653f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **260.3 MB (260323511 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83ad04a1beb18b02eb6837cab4ce13d00614fd5c100fcb38161937959aa16b7a`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1765152000'
# Tue, 16 Dec 2025 00:04:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 16 Dec 2025 00:04:21 GMT
ENV JAVA_HOME=/usr/local/openjdk-27
# Tue, 16 Dec 2025 00:04:21 GMT
ENV PATH=/usr/local/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Dec 2025 00:04:21 GMT
ENV LANG=C.UTF-8
# Tue, 16 Dec 2025 00:04:21 GMT
ENV JAVA_VERSION=27-ea+2
# Tue, 16 Dec 2025 00:04:21 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/2/GPL/openjdk-27-ea+2_linux-x64_bin.tar.gz'; 			downloadSha256='95b0225ac04e0034ffe1626daf09cf436a54ac3b74fef67ccd00534beb7715f5'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/2/GPL/openjdk-27-ea+2_linux-aarch64_bin.tar.gz'; 			downloadSha256='111a65a5acf09c18b471be75d77130d10b4c425d192ae243e3940da32e5d6dca'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 16 Dec 2025 00:04:21 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1733a4cd59540b3470ff7a90963bcdea5b543279dd6bdaf022d7883fdad221e5`  
		Last Modified: Mon, 08 Dec 2025 22:17:58 GMT  
		Size: 29.8 MB (29776496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3a342383315c11cf3d82ef19d77cd2721e5ae718ba14f05f9ac4fe6cbe1ca14`  
		Last Modified: Tue, 16 Dec 2025 00:04:55 GMT  
		Size: 2.4 MB (2370988 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9a6a577adcdcb40d960090f04e7ac879f5a6934f2a50c2f6e6f9fbef2314880`  
		Last Modified: Tue, 16 Dec 2025 00:06:41 GMT  
		Size: 228.2 MB (228176027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-2-jdk-slim-trixie` - unknown; unknown

```console
$ docker pull openjdk@sha256:912520d0f12b1641f61ba479b3620b32248d65f1d6eb117a0dad25d32344609a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2296863 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a85b544b40e273ab888f5f21ff24f9ebe79b4b9c01c62f6fbcd46646f46e91de`

```dockerfile
```

-	Layers:
	-	`sha256:41f234617e55e9f9e329c9baca9f6e273305c4d40d2cd63ddcacf56624223235`  
		Last Modified: Tue, 16 Dec 2025 01:26:20 GMT  
		Size: 2.3 MB (2278775 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2b49ce0faaaacac4e8995d009ba9691e833f924d1853f4a2664d966d7b45dc93`  
		Last Modified: Tue, 16 Dec 2025 01:26:20 GMT  
		Size: 18.1 KB (18088 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:27-ea-2-jdk-slim-trixie` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:84256e000391bec200c6f631df39d1d6e3fcbf5898447ac8818c0e1bd70bb306
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.6 MB (258553411 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b5c128ef327c92d676c04357b97ac4355f5ee4b6fb9b010b74adf108cfbc2c3`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1765152000'
# Tue, 16 Dec 2025 00:03:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 16 Dec 2025 00:04:07 GMT
ENV JAVA_HOME=/usr/local/openjdk-27
# Tue, 16 Dec 2025 00:04:07 GMT
ENV PATH=/usr/local/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Dec 2025 00:04:07 GMT
ENV LANG=C.UTF-8
# Tue, 16 Dec 2025 00:04:07 GMT
ENV JAVA_VERSION=27-ea+2
# Tue, 16 Dec 2025 00:04:07 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/2/GPL/openjdk-27-ea+2_linux-x64_bin.tar.gz'; 			downloadSha256='95b0225ac04e0034ffe1626daf09cf436a54ac3b74fef67ccd00534beb7715f5'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/2/GPL/openjdk-27-ea+2_linux-aarch64_bin.tar.gz'; 			downloadSha256='111a65a5acf09c18b471be75d77130d10b4c425d192ae243e3940da32e5d6dca'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 16 Dec 2025 00:04:07 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f626fba1463b32b20f78d29b52dcf15be927dbb5372a9ba6a5f97aad47ae220b`  
		Last Modified: Mon, 08 Dec 2025 22:17:19 GMT  
		Size: 30.1 MB (30138628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3f87af12f3129c13fe4ad84c8275bed3037d0b9c0884e78a9adbe877d0ee943`  
		Last Modified: Tue, 16 Dec 2025 00:04:39 GMT  
		Size: 2.3 MB (2314092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cbe36c6fbcd48d3d4aae5579bf329836d122fccaa9f4413f9dd0b98c4c96e5b`  
		Last Modified: Tue, 16 Dec 2025 00:05:07 GMT  
		Size: 226.1 MB (226100691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-2-jdk-slim-trixie` - unknown; unknown

```console
$ docker pull openjdk@sha256:ef2469d5d0f2233ce0955cca704a53377af15dcd78defb13433e287976fa0237
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2296716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ce5ced7443c26950a7ae2da97a38a582b1e8115ffcb70664805b404ed55b498`

```dockerfile
```

-	Layers:
	-	`sha256:3436c9c8619f55342036d6239f4ba43221e764845b6a345936709f37d9bdc151`  
		Last Modified: Tue, 16 Dec 2025 01:26:24 GMT  
		Size: 2.3 MB (2278461 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e1e39d367fba15a7870a0d855c79f7697d5ff778dae06fddddbbf898474197d3`  
		Last Modified: Tue, 16 Dec 2025 01:26:25 GMT  
		Size: 18.3 KB (18255 bytes)  
		MIME: application/vnd.in-toto+json
