## `openjdk:27-ea-slim-bookworm`

```console
$ docker pull openjdk@sha256:78605390ff02b4b0f87e95420f6bc37f9d2c85944724ac303a1c8ab75dbe8c7e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:27-ea-slim-bookworm` - linux; amd64

```console
$ docker pull openjdk@sha256:c3f35622727a0a41fd6c8fe4555bb2579a65f2242332d3f237944ad374de72b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **260.8 MB (260811458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f5ab7309b0024bee7ea8e3f1c88b47a9786dd2b4efe3d45bbaf50de91aba2f1`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1769990400'
# Sat, 21 Feb 2026 01:29:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 21 Feb 2026 01:29:28 GMT
ENV JAVA_HOME=/usr/local/openjdk-27
# Sat, 21 Feb 2026 01:29:28 GMT
ENV PATH=/usr/local/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 21 Feb 2026 01:29:28 GMT
ENV LANG=C.UTF-8
# Sat, 21 Feb 2026 01:29:28 GMT
ENV JAVA_VERSION=27-ea+10
# Sat, 21 Feb 2026 01:29:28 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/10/GPL/openjdk-27-ea+10_linux-x64_bin.tar.gz'; 			downloadSha256='d42a6202d27fdca3cc1de29d07dc85bb73d27637ba1e1ed715357472da050d31'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/10/GPL/openjdk-27-ea+10_linux-aarch64_bin.tar.gz'; 			downloadSha256='91f6dae354fee821c0052fdbe9acd9f894976596733268741b65d4a4a25ec686'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 21 Feb 2026 01:29:28 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:4831516dd0cb86845f5f902cb9b9d25b5c853152c337eb57e4737a9b7e2a2eb9`  
		Last Modified: Tue, 03 Feb 2026 01:13:33 GMT  
		Size: 28.2 MB (28228487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43c4d4830391d7e784245089f4acee703bb5113a5476974e120630f81d7f20ab`  
		Last Modified: Sat, 21 Feb 2026 01:29:48 GMT  
		Size: 4.0 MB (4029282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2da7e40155c934a0e59d7125af155f86113825a5ac793662b92a49b8afe3a86e`  
		Last Modified: Sat, 21 Feb 2026 01:29:54 GMT  
		Size: 228.6 MB (228553689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-slim-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:52fa17b878c517cf1c6077d50658b7b35de9429a6186986156e8bb28c1fe6ce4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2666675 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ca41935eca4f3fe19cbb3e350d993c32ae30f040df0f13a842bbaf15f8ec446`

```dockerfile
```

-	Layers:
	-	`sha256:bfe77056c0592c09175d4e22a6178a2060fe4fc8b9925534f848e132a50af69b`  
		Last Modified: Sat, 21 Feb 2026 01:29:48 GMT  
		Size: 2.6 MB (2649805 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a5a4f81eb7be0b53cc3de9b631ee9ff3fb52025bd6270fefa101c5dd669cc9f4`  
		Last Modified: Sat, 21 Feb 2026 01:29:48 GMT  
		Size: 16.9 KB (16870 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:27-ea-slim-bookworm` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:6c4fc04dc99ea31652528ee48f4350b35170127e0c3a921c60481384797fa009
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.5 MB (258463112 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:059f4326fc77aac58327c05a1c4667677b8e46036745cf9b739c4a2eab552645`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1769990400'
# Sat, 21 Feb 2026 01:29:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 21 Feb 2026 01:29:28 GMT
ENV JAVA_HOME=/usr/local/openjdk-27
# Sat, 21 Feb 2026 01:29:28 GMT
ENV PATH=/usr/local/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 21 Feb 2026 01:29:28 GMT
ENV LANG=C.UTF-8
# Sat, 21 Feb 2026 01:29:28 GMT
ENV JAVA_VERSION=27-ea+10
# Sat, 21 Feb 2026 01:29:28 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/10/GPL/openjdk-27-ea+10_linux-x64_bin.tar.gz'; 			downloadSha256='d42a6202d27fdca3cc1de29d07dc85bb73d27637ba1e1ed715357472da050d31'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/10/GPL/openjdk-27-ea+10_linux-aarch64_bin.tar.gz'; 			downloadSha256='91f6dae354fee821c0052fdbe9acd9f894976596733268741b65d4a4a25ec686'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 21 Feb 2026 01:29:28 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:d3d5d8ab26d25b9040a3c2160d7ddfe3911ae81035d5b1b0904f3ebda32476b6`  
		Last Modified: Tue, 03 Feb 2026 01:13:36 GMT  
		Size: 28.1 MB (28107823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8519566d92d5e3806817b3adb72ce9792d4dcfc9d2aafab3fb97ce6d5640c2f8`  
		Last Modified: Sat, 21 Feb 2026 01:29:50 GMT  
		Size: 3.9 MB (3851970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c58c4d0ec9ba5c55ebbb1c014ce86d8ab56103d6a50ed4efcfcf8c460e922290`  
		Last Modified: Sat, 21 Feb 2026 01:29:54 GMT  
		Size: 226.5 MB (226503319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-slim-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:e323f4b9265993627e8230c1d026da30b5e7c6ee49774ad82cf7dee65e829253
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2666429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26e9e5e6a6f02ca6412288c8eff7ffa85398e5822877f0239d272f1024c87a04`

```dockerfile
```

-	Layers:
	-	`sha256:955705a4cfca22e587ae11be70f8684c76c91c7e58391d0789ddb3934ea2a262`  
		Last Modified: Sat, 21 Feb 2026 01:29:49 GMT  
		Size: 2.6 MB (2649439 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fb7b39fb3c3bbc39a674c6157896a51b6351bab98d149b07bd8cdf31dff169cb`  
		Last Modified: Sat, 21 Feb 2026 01:29:49 GMT  
		Size: 17.0 KB (16990 bytes)  
		MIME: application/vnd.in-toto+json
