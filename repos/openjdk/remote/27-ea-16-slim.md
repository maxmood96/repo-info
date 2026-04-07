## `openjdk:27-ea-16-slim`

```console
$ docker pull openjdk@sha256:43f3a534ac830be97384ce34abd244cee7b9da1c61416d06444981e60dde7de8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:27-ea-16-slim` - linux; amd64

```console
$ docker pull openjdk@sha256:ff35c290d76fd875046d642f9033d8169907b0bdadc28edb3f876924a976c7a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.1 MB (261107599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6233d0dce2fec14ca0c91abff3b3d2370080be7c1432811df3203f4b2b4bfb2`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 02:02:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:02:57 GMT
ENV JAVA_HOME=/usr/local/openjdk-27
# Tue, 07 Apr 2026 02:02:57 GMT
ENV PATH=/usr/local/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 02:02:57 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 02:02:57 GMT
ENV JAVA_VERSION=27-ea+16
# Tue, 07 Apr 2026 02:02:57 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/16/GPL/openjdk-27-ea+16_linux-x64_bin.tar.gz'; 			downloadSha256='a9c8f46b87d1c973c4749728845de23d38a1897dc78b85e362f76ce98ca826eb'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/16/GPL/openjdk-27-ea+16_linux-aarch64_bin.tar.gz'; 			downloadSha256='cc96a894335065d7218341881222321567d1eca6950b3d6433fc387295d8d3b0'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 07 Apr 2026 02:02:57 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:5435b2dcdf5cb7faa0d5b1d4d54be2c72a776fab9a605336f5067d6e9ecb5976`  
		Last Modified: Tue, 07 Apr 2026 00:11:35 GMT  
		Size: 29.8 MB (29775640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa3f8b77af7a40a2c890e1bc566d11d4426fe4e1a2e8f58d1643185705fb4ed7`  
		Last Modified: Tue, 07 Apr 2026 02:03:15 GMT  
		Size: 2.4 MB (2371147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87de6d44428c2c56726ac45be2c6f717272a3062e6a1e69cd65ff6e775fa5ed6`  
		Last Modified: Tue, 07 Apr 2026 02:03:19 GMT  
		Size: 229.0 MB (228960812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-16-slim` - unknown; unknown

```console
$ docker pull openjdk@sha256:f4a171d76ef6e19616e67714c0eaae398619cb0a315ccfce31e9dcf04bf69ebf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2297004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13a9fc8be43d30a95db25bd9e45cc656ff4ccc874dd8dd8a9eb1c3b645588785`

```dockerfile
```

-	Layers:
	-	`sha256:a627f6254284aa5cc9bc3eccb5d401a3523c33f8980a8d3468e4c1f4d0fda6fd`  
		Last Modified: Tue, 07 Apr 2026 02:03:15 GMT  
		Size: 2.3 MB (2278895 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0050fff6e249f48681e02acc1e20eb7c4a0494a3a0a17e6f5253b6e670c15604`  
		Last Modified: Tue, 07 Apr 2026 02:03:15 GMT  
		Size: 18.1 KB (18109 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:27-ea-16-slim` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:828c0b49e4876d4bc72ecd78c9bb71af8ddda2ac162ce331b3b1914010402222
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **259.4 MB (259380607 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61764b31cc628a352223189b9e37f85fc489268ee1ee1a59532e9a53d982e32b`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 02:05:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:05:57 GMT
ENV JAVA_HOME=/usr/local/openjdk-27
# Tue, 07 Apr 2026 02:05:57 GMT
ENV PATH=/usr/local/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 02:05:57 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 02:05:57 GMT
ENV JAVA_VERSION=27-ea+16
# Tue, 07 Apr 2026 02:05:57 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/16/GPL/openjdk-27-ea+16_linux-x64_bin.tar.gz'; 			downloadSha256='a9c8f46b87d1c973c4749728845de23d38a1897dc78b85e362f76ce98ca826eb'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/16/GPL/openjdk-27-ea+16_linux-aarch64_bin.tar.gz'; 			downloadSha256='cc96a894335065d7218341881222321567d1eca6950b3d6433fc387295d8d3b0'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 07 Apr 2026 02:05:57 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:53196b1f47bdd6997874156c61491c9a36e115d9b7bd5d74e0cb5c2fc4ee69ce`  
		Last Modified: Tue, 07 Apr 2026 00:11:28 GMT  
		Size: 30.1 MB (30138551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abbe6162f3d17dac5805eb2f90e5b6ec0089d8290791838c1301d3cb09c6bb74`  
		Last Modified: Tue, 07 Apr 2026 02:06:18 GMT  
		Size: 2.3 MB (2314422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1eb2a78f84abf2a4e501303b79549ff45fb4004bd4035b333271208240359850`  
		Last Modified: Tue, 07 Apr 2026 02:06:22 GMT  
		Size: 226.9 MB (226927634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-16-slim` - unknown; unknown

```console
$ docker pull openjdk@sha256:dd7c46778e2cae5e7d79ac3de537c99c80dd429d14cd8ef586bacae38200dc2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2296857 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7163e034bf5033dafdab5239ec659b3880cb5d8768508b505d5253f57af6f11`

```dockerfile
```

-	Layers:
	-	`sha256:4100188015e161653030e2682ceb26911d1216e280cb8933780c73617bccb813`  
		Last Modified: Tue, 07 Apr 2026 02:06:17 GMT  
		Size: 2.3 MB (2278581 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8934f91123e41cb7368969c7aab3e7fcb4ff5a4b721f2fbe551f706633f2ee3f`  
		Last Modified: Tue, 07 Apr 2026 02:06:17 GMT  
		Size: 18.3 KB (18276 bytes)  
		MIME: application/vnd.in-toto+json
