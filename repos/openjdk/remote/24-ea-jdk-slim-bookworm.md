## `openjdk:24-ea-jdk-slim-bookworm`

```console
$ docker pull openjdk@sha256:7454003c7a917535aeb4c1afd0f910c30e9eb53c08621a4b5920ac6900b44ba8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:24-ea-jdk-slim-bookworm` - linux; amd64

```console
$ docker pull openjdk@sha256:a039e3e26f025bf1e5ea20cb675f7fcf1f789741d256bd5812e9f08a06439410
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **245.0 MB (244973748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:846708cca3f0c4a52ce12674088f3eba479e1eee159451c3d4af609e33e23355`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 23 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1734912000'
# Fri, 10 Jan 2025 07:48:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 10 Jan 2025 07:48:13 GMT
ENV JAVA_HOME=/usr/local/openjdk-24
# Fri, 10 Jan 2025 07:48:13 GMT
ENV PATH=/usr/local/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 10 Jan 2025 07:48:13 GMT
ENV LANG=C.UTF-8
# Fri, 10 Jan 2025 07:48:13 GMT
ENV JAVA_VERSION=24-ea+31
# Fri, 10 Jan 2025 07:48:13 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/31/GPL/openjdk-24-ea+31_linux-x64_bin.tar.gz'; 			downloadSha256='fc69771e3af411ad5be33bf328a73b32318264a7aef1f28d1e6339cbf609819b'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/31/GPL/openjdk-24-ea+31_linux-aarch64_bin.tar.gz'; 			downloadSha256='5c35cd6370cdbe71bda96ccae35f3a74972b83dc6958e783b803f730b24f9a0a'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 10 Jan 2025 07:48:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:fd674058ff8f8cfa7fb8a20c006fc0128541cbbad7f7f7f28df570d08f9e4d92`  
		Last Modified: Tue, 24 Dec 2024 21:32:20 GMT  
		Size: 28.2 MB (28231581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cdbeba1919e2976e4273f7b93fc678b9471c8faaec4cbf537f691e9ec820651`  
		Last Modified: Sat, 11 Jan 2025 02:29:45 GMT  
		Size: 3.8 MB (3824687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0a97b937d77da574da0adbd2136d1ac5b81a232827313cd38b6633e0b458929`  
		Last Modified: Sat, 11 Jan 2025 02:29:48 GMT  
		Size: 212.9 MB (212917480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-ea-jdk-slim-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:542f3dea4bd0970829d452d5d3ad7b37f96030a7ad63777db4499704b4e7d944
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2553960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca885a67613c14ce60825a981cefb3d9a469aa505a7e7cd4d63fbbe3981d9b3c`

```dockerfile
```

-	Layers:
	-	`sha256:e08a4382ccca7e71536ec77f96bef31162397652071007ffde179f0293768355`  
		Last Modified: Sat, 11 Jan 2025 02:29:45 GMT  
		Size: 2.5 MB (2534519 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:054fb5758c47ac07d0d7b0118bb76eda4494b2c2cb26e1a98c9280f7a5a7acc9`  
		Last Modified: Sat, 11 Jan 2025 02:29:45 GMT  
		Size: 19.4 KB (19441 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:24-ea-jdk-slim-bookworm` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:d934c9da2f0460061e6dcd45f0fb9614da4ab508523ec9de288dc57ebf06fca8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.6 MB (242581602 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fd7c04f6727cd09b8c6fa219738c59a86b9d4706ed3883a4856632a2d9179a2`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 23 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1734912000'
# Fri, 10 Jan 2025 07:48:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 10 Jan 2025 07:48:13 GMT
ENV JAVA_HOME=/usr/local/openjdk-24
# Fri, 10 Jan 2025 07:48:13 GMT
ENV PATH=/usr/local/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 10 Jan 2025 07:48:13 GMT
ENV LANG=C.UTF-8
# Fri, 10 Jan 2025 07:48:13 GMT
ENV JAVA_VERSION=24-ea+31
# Fri, 10 Jan 2025 07:48:13 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/31/GPL/openjdk-24-ea+31_linux-x64_bin.tar.gz'; 			downloadSha256='fc69771e3af411ad5be33bf328a73b32318264a7aef1f28d1e6339cbf609819b'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/31/GPL/openjdk-24-ea+31_linux-aarch64_bin.tar.gz'; 			downloadSha256='5c35cd6370cdbe71bda96ccae35f3a74972b83dc6958e783b803f730b24f9a0a'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 10 Jan 2025 07:48:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f5c6876bb3d7d368455916fa98c705330bd8a8d9c080ccea8fe4c4b35a2ecb1f`  
		Last Modified: Tue, 24 Dec 2024 21:34:20 GMT  
		Size: 28.1 MB (28058723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac6ff135ed08a1ea8c79c626a6c19f1b6f682176f521b40dbddaa1bbe09b4fd9`  
		Last Modified: Sat, 11 Jan 2025 03:17:53 GMT  
		Size: 3.6 MB (3639390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea1ea83e745618b009f8c7ade081ed1a47eee690b64731cbd008d31edd4fa968`  
		Last Modified: Sat, 11 Jan 2025 03:23:35 GMT  
		Size: 210.9 MB (210883489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-ea-jdk-slim-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:272449fdfb626324f6914f5a0bc8fea5a851902d5ad8d5937fb7c4c0eccda22e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2553906 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:966c7a687cc7e5341b9a2c55ea264a45b99c4a51d876974f84b8d69a5b6e3ec1`

```dockerfile
```

-	Layers:
	-	`sha256:8ffeffc6a469aef564e33fc667bdf9249aac1a86d0aa3e64e2c5ac20aa7d2c7c`  
		Last Modified: Sat, 11 Jan 2025 03:23:29 GMT  
		Size: 2.5 MB (2534249 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:13764d8db3680a690681fae91fea37de6d1e975d767eaa7a8064f31a1fba801e`  
		Last Modified: Sat, 11 Jan 2025 03:23:29 GMT  
		Size: 19.7 KB (19657 bytes)  
		MIME: application/vnd.in-toto+json
