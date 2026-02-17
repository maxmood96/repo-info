## `openjdk:26-rc-slim`

```console
$ docker pull openjdk@sha256:2ac49993f322de5831bc964569ec2d396245fc2ee104f13c49bdfeaa768072a3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:26-rc-slim` - linux; amd64

```console
$ docker pull openjdk@sha256:d7e3c861e5ff566f70afdefc6b2f8b7c5451ec38043ec9ffb375426bd6497a82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **260.3 MB (260258732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97d3d046c321aa90aea2963928701d047753287d0a031ea44ea4bcc84473976f`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1769990400'
# Tue, 17 Feb 2026 19:30:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 19:30:53 GMT
ENV JAVA_HOME=/usr/local/openjdk-26
# Tue, 17 Feb 2026 19:30:53 GMT
ENV PATH=/usr/local/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 19:30:53 GMT
ENV LANG=C.UTF-8
# Tue, 17 Feb 2026 19:30:53 GMT
ENV JAVA_VERSION=26
# Tue, 17 Feb 2026 19:30:53 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/GA/jdk26/c3cc523845074aa0af4f5e1e1ed4151d/35/GPL/openjdk-26_linux-x64_bin.tar.gz'; 			downloadSha256='83c78367f8c81257beef72aca4bbbf8e6dac8ca2b3a4546a85879a09e6e4e128'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/GA/jdk26/c3cc523845074aa0af4f5e1e1ed4151d/35/GPL/openjdk-26_linux-aarch64_bin.tar.gz'; 			downloadSha256='403ccf451e88d0be9e1dec129fcb9318de9752121e0eb92dfa9a8cf06f249007'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 17 Feb 2026 19:30:53 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:0c8d55a45c0dc58de60579b9cc5b708de9e7957f4591fc7de941b67c7e245da0`  
		Last Modified: Tue, 03 Feb 2026 01:15:17 GMT  
		Size: 29.8 MB (29778596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc70d015116ab59572e571ce6b0813cc555594cd62d913834a1f3b4c5a2359a0`  
		Last Modified: Tue, 17 Feb 2026 19:31:12 GMT  
		Size: 2.4 MB (2371015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcd47cc284320bd9eccb92e8f8ec8e924b390e907f3a9f0adf1cf90e3899e93f`  
		Last Modified: Tue, 17 Feb 2026 19:31:16 GMT  
		Size: 228.1 MB (228109121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-rc-slim` - unknown; unknown

```console
$ docker pull openjdk@sha256:df8fba271875e70bd2772bd7e6f099700429dc2415b9c40f2bc52417845d3a69
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2295041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:403a29844ecbb34f706830ac0ab1593e37b7b33b4dbccedbbbe91606903c0a65`

```dockerfile
```

-	Layers:
	-	`sha256:764d79e2bcae598f742ae2d9a08cfdae2fba15f59e5799696f7e4e6720656907`  
		Last Modified: Tue, 17 Feb 2026 19:31:12 GMT  
		Size: 2.3 MB (2278168 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eb1164df072134bd94e3a0f027d8eaa2befabf38ad41ca584db17e614d01fad7`  
		Last Modified: Tue, 17 Feb 2026 19:31:12 GMT  
		Size: 16.9 KB (16873 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:26-rc-slim` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:13beaeda3e99ddb46d46bd77abe94e6202cf2a17bc800026384b164312fab6b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.5 MB (258490068 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fffb18da4c557e9c9398a4c4aef41a59b42102897e5a7fc60f3e9cfcd3f36761`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1769990400'
# Tue, 17 Feb 2026 19:29:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 19:30:03 GMT
ENV JAVA_HOME=/usr/local/openjdk-26
# Tue, 17 Feb 2026 19:30:03 GMT
ENV PATH=/usr/local/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 19:30:03 GMT
ENV LANG=C.UTF-8
# Tue, 17 Feb 2026 19:30:03 GMT
ENV JAVA_VERSION=26
# Tue, 17 Feb 2026 19:30:03 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/GA/jdk26/c3cc523845074aa0af4f5e1e1ed4151d/35/GPL/openjdk-26_linux-x64_bin.tar.gz'; 			downloadSha256='83c78367f8c81257beef72aca4bbbf8e6dac8ca2b3a4546a85879a09e6e4e128'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/GA/jdk26/c3cc523845074aa0af4f5e1e1ed4151d/35/GPL/openjdk-26_linux-aarch64_bin.tar.gz'; 			downloadSha256='403ccf451e88d0be9e1dec129fcb9318de9752121e0eb92dfa9a8cf06f249007'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 17 Feb 2026 19:30:03 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3ea009573b472d108af9af31ec35a06fe3649084f6611cf11f7d594b85cf7a7c`  
		Last Modified: Tue, 03 Feb 2026 01:15:22 GMT  
		Size: 30.1 MB (30140064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:845f7b0d5e87f75269977138dae44567063d678b3ae59d1b711756efcd69adcb`  
		Last Modified: Tue, 17 Feb 2026 19:30:26 GMT  
		Size: 2.3 MB (2314389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63c49b74058c4dd9d992bd1c39e6dcb592c5aba643ae5dbba8c84890329b7d76`  
		Last Modified: Tue, 17 Feb 2026 19:30:30 GMT  
		Size: 226.0 MB (226035615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-rc-slim` - unknown; unknown

```console
$ docker pull openjdk@sha256:fe6b41fe563e1091fe0edbe9ea46c04b0e42098b4468aa21542a981a57477212
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2294798 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:628e0f20716826d9b1fec70eb17853c7899befb0f85783124a8640033286a285`

```dockerfile
```

-	Layers:
	-	`sha256:39595dc88d5178b4e3f12bb1a764c4c029b822a8e358b8cbe30d68cd45e27686`  
		Last Modified: Tue, 17 Feb 2026 19:30:26 GMT  
		Size: 2.3 MB (2277806 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:00869186c23b6d172fd7bea1a7723fd665bbcee67f8b3463a166b01849e8a72f`  
		Last Modified: Tue, 17 Feb 2026 19:30:26 GMT  
		Size: 17.0 KB (16992 bytes)  
		MIME: application/vnd.in-toto+json
