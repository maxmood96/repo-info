## `openjdk:26-rc-slim-trixie`

```console
$ docker pull openjdk@sha256:20167aa68ce3fe1f0a26b4795811e1c56d69fbbe587db86da976c3c10659ab25
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:26-rc-slim-trixie` - linux; amd64

```console
$ docker pull openjdk@sha256:6b215d676edbfc9c7d37172b4b71cd7b5879e008cd943a7e7677f2e50abdc377
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **260.2 MB (260185259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0da4eb476c57977700ee03e60e167c9789f3d62a1d78f10939f99fa10be6660`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1769990400'
# Thu, 12 Feb 2026 23:59:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 13 Feb 2026 00:00:11 GMT
ENV JAVA_HOME=/usr/local/openjdk-26
# Fri, 13 Feb 2026 00:00:11 GMT
ENV PATH=/usr/local/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 13 Feb 2026 00:00:11 GMT
ENV LANG=C.UTF-8
# Fri, 13 Feb 2026 00:00:11 GMT
ENV JAVA_VERSION=26
# Fri, 13 Feb 2026 00:00:11 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/GA/jdk26/c3cc523845074aa0af4f5e1e1ed4151d/34/GPL/openjdk-26_linux-x64_bin.tar.gz'; 			downloadSha256='e7c907ec1036e5480609f8212e6f1e7f710310e029d097e4e1a9645c43676945'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/GA/jdk26/c3cc523845074aa0af4f5e1e1ed4151d/34/GPL/openjdk-26_linux-aarch64_bin.tar.gz'; 			downloadSha256='aeb9ccc00550a012197834334a9a6cbc03e7938774fcaf59dfa7ed158b66465f'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 13 Feb 2026 00:00:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:0c8d55a45c0dc58de60579b9cc5b708de9e7957f4591fc7de941b67c7e245da0`  
		Last Modified: Tue, 03 Feb 2026 01:15:17 GMT  
		Size: 29.8 MB (29778596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c3b70499187a15f70241ac06cbb1927ce3546302ed635f7c0554600862836c7`  
		Last Modified: Fri, 13 Feb 2026 00:00:32 GMT  
		Size: 2.4 MB (2371031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:737c8d95ad6a5dd047f8cfe98a75a3dadf3d996dad546bbff0aab35166697ded`  
		Last Modified: Fri, 13 Feb 2026 00:00:37 GMT  
		Size: 228.0 MB (228035632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-rc-slim-trixie` - unknown; unknown

```console
$ docker pull openjdk@sha256:80fba9ffce42b0be4efad70c623d8064c496a350e273aed35be8f416ca8d833b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2294412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d90eca0ecf9d6d8b85190a370154cb8a450aabdfc0af9a7e484f694bc707b2db`

```dockerfile
```

-	Layers:
	-	`sha256:be4030e3d987dd89dab2544dca607e4145adc3dc76196c49d65ce49cf2c040dd`  
		Last Modified: Fri, 13 Feb 2026 00:00:32 GMT  
		Size: 2.3 MB (2277539 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:04585ff3ad960490df33ba94621db52f2906dd5d6b3ed4af6bfb78305c29e6e7`  
		Last Modified: Fri, 13 Feb 2026 00:00:32 GMT  
		Size: 16.9 KB (16873 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:26-rc-slim-trixie` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:cc7e744cdfdf684b224743c8dc8cb2f456ab5f7d6e7a11f870769ecc4399966b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.4 MB (258404913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:786308299d84c6d95168f14d9f9ab6c79e789a50e0d4ae4cc1e81c5ff9401f37`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1769990400'
# Fri, 13 Feb 2026 00:02:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 13 Feb 2026 00:02:45 GMT
ENV JAVA_HOME=/usr/local/openjdk-26
# Fri, 13 Feb 2026 00:02:45 GMT
ENV PATH=/usr/local/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 13 Feb 2026 00:02:45 GMT
ENV LANG=C.UTF-8
# Fri, 13 Feb 2026 00:02:45 GMT
ENV JAVA_VERSION=26
# Fri, 13 Feb 2026 00:02:45 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/GA/jdk26/c3cc523845074aa0af4f5e1e1ed4151d/34/GPL/openjdk-26_linux-x64_bin.tar.gz'; 			downloadSha256='e7c907ec1036e5480609f8212e6f1e7f710310e029d097e4e1a9645c43676945'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/GA/jdk26/c3cc523845074aa0af4f5e1e1ed4151d/34/GPL/openjdk-26_linux-aarch64_bin.tar.gz'; 			downloadSha256='aeb9ccc00550a012197834334a9a6cbc03e7938774fcaf59dfa7ed158b66465f'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 13 Feb 2026 00:02:45 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3ea009573b472d108af9af31ec35a06fe3649084f6611cf11f7d594b85cf7a7c`  
		Last Modified: Tue, 03 Feb 2026 01:15:22 GMT  
		Size: 30.1 MB (30140064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5381d665720feb561e80387fd93916696b8959909361d15c34b493cd650506c7`  
		Last Modified: Fri, 13 Feb 2026 00:03:06 GMT  
		Size: 2.3 MB (2314428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adfe76de5bf4e872effc3933c541f37843eff198c2e0b9276599937c531872f8`  
		Last Modified: Fri, 13 Feb 2026 00:03:11 GMT  
		Size: 226.0 MB (225950421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-rc-slim-trixie` - unknown; unknown

```console
$ docker pull openjdk@sha256:ea2a17a2c78c1abc4df83d21812af0513a209ef851e7165892ea31bc5f39870c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2294169 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91b21799b40d2a279378f33336ed347117778516bc5ce5da4101ba670f5bb565`

```dockerfile
```

-	Layers:
	-	`sha256:6f7a99fbc03cd0001901335a4b1dcf852b0a106bb1302684d46f2d19e961f72e`  
		Last Modified: Fri, 13 Feb 2026 00:03:06 GMT  
		Size: 2.3 MB (2277177 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:63988ab4486ab9a6e276c497b7e09877268ea22bf78c8a9393b8d0698fb69764`  
		Last Modified: Fri, 13 Feb 2026 00:03:06 GMT  
		Size: 17.0 KB (16992 bytes)  
		MIME: application/vnd.in-toto+json
