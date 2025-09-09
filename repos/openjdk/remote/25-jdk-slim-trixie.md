## `openjdk:25-jdk-slim-trixie`

```console
$ docker pull openjdk@sha256:4d9bb48a3d5c2015a5e67eeab7575b6b11eda252aee651e632ef57d24aaf2d82
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:25-jdk-slim-trixie` - linux; amd64

```console
$ docker pull openjdk@sha256:988f9f2e77fc48ef3c81fc429d56110c6f43c35b43493f843f98bb21c6f75333
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.4 MB (255380990 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2261f15ca472f243c383c62e28ce5ded9022191d8ff09394b558e799df85f6e1`
-	Default Command: `["jshell"]`

```dockerfile
# Sat, 16 Aug 2025 00:48:25 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1757289600'
# Sat, 16 Aug 2025 00:48:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 16 Aug 2025 00:48:25 GMT
ENV JAVA_HOME=/usr/local/openjdk-25
# Sat, 16 Aug 2025 00:48:25 GMT
ENV PATH=/usr/local/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 16 Aug 2025 00:48:25 GMT
ENV LANG=C.UTF-8
# Sat, 16 Aug 2025 00:48:25 GMT
ENV JAVA_VERSION=25
# Sat, 16 Aug 2025 00:48:25 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/GA/jdk25/bd75d5f9689641da8e1daabeccb5528b/36/GPL/openjdk-25_linux-x64_bin.tar.gz'; 			downloadSha256='59cdcaf255add4721de38eb411d4ecfe779356b61fb671aee63c7dec78054c2b'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/GA/jdk25/bd75d5f9689641da8e1daabeccb5528b/36/GPL/openjdk-25_linux-aarch64_bin.tar.gz'; 			downloadSha256='f4a8d27429458a529148f90ebafcd1ae9b1968fa323f9e5e40d579a5c8c0288f'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 16 Aug 2025 00:48:25 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:ce1261c6d567efa8e3b457673eeeb474a0a8066df6bb95ca9a6a94a31e219dd3`  
		Last Modified: Mon, 08 Sep 2025 21:12:35 GMT  
		Size: 29.8 MB (29773495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a47ed5d1b6e6125e0fb2140a7303541bc8624183bd910380306a7d2c7172ab8`  
		Last Modified: Mon, 08 Sep 2025 21:47:11 GMT  
		Size: 2.4 MB (2371140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1ea9f662972e8a6dca391f152b7774ca9d415f82b85a722210057ccd57d7769`  
		Last Modified: Mon, 08 Sep 2025 22:12:41 GMT  
		Size: 223.2 MB (223236355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-jdk-slim-trixie` - unknown; unknown

```console
$ docker pull openjdk@sha256:1430fde398eca55a34c11b9f24bc7af2c3dafb99d8fb89a4181cf7c3e3c16ef4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2299998 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:201018ff2f40bfda1d4da8ed9057afa2ada45a9496fe898f9d85baf411ab80c9`

```dockerfile
```

-	Layers:
	-	`sha256:4c221c3a92babf82d9fc0cb61b65a84129c15b683562d21aa6a048e317524ed4`  
		Last Modified: Tue, 09 Sep 2025 00:23:32 GMT  
		Size: 2.3 MB (2281822 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3649ed5d7f7f668b9fb61c083603cf7c94474edd4ff5c2e9611dec5095a4fc9a`  
		Last Modified: Tue, 09 Sep 2025 00:23:33 GMT  
		Size: 18.2 KB (18176 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:25-jdk-slim-trixie` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:babd96b199521b42faa5afd67c9496f12effbecd8571e52da742d9ba4684ee6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.5 MB (253483860 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:788898fcf7cf66397751052187fab74f56821eb3a18d0c1374256abd47f525f8`
-	Default Command: `["jshell"]`

```dockerfile
# Sat, 16 Aug 2025 00:48:25 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1757289600'
# Sat, 16 Aug 2025 00:48:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 16 Aug 2025 00:48:25 GMT
ENV JAVA_HOME=/usr/local/openjdk-25
# Sat, 16 Aug 2025 00:48:25 GMT
ENV PATH=/usr/local/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 16 Aug 2025 00:48:25 GMT
ENV LANG=C.UTF-8
# Sat, 16 Aug 2025 00:48:25 GMT
ENV JAVA_VERSION=25
# Sat, 16 Aug 2025 00:48:25 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/GA/jdk25/bd75d5f9689641da8e1daabeccb5528b/36/GPL/openjdk-25_linux-x64_bin.tar.gz'; 			downloadSha256='59cdcaf255add4721de38eb411d4ecfe779356b61fb671aee63c7dec78054c2b'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/GA/jdk25/bd75d5f9689641da8e1daabeccb5528b/36/GPL/openjdk-25_linux-aarch64_bin.tar.gz'; 			downloadSha256='f4a8d27429458a529148f90ebafcd1ae9b1968fa323f9e5e40d579a5c8c0288f'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 16 Aug 2025 00:48:25 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:b2feff975e6dd2ebaf182772fb9ee26274648387b061e821e0bb5026735dd094`  
		Last Modified: Mon, 08 Sep 2025 21:13:54 GMT  
		Size: 30.1 MB (30136631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbc389582902da84604490108c2324a79d78fec1111752006003c021e131bff8`  
		Last Modified: Mon, 08 Sep 2025 22:04:07 GMT  
		Size: 2.3 MB (2314274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91aaf51f21639634b522b0b0faff673898c252273cf2b9572f069f0374b38569`  
		Last Modified: Tue, 09 Sep 2025 00:50:03 GMT  
		Size: 221.0 MB (221032955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-jdk-slim-trixie` - unknown; unknown

```console
$ docker pull openjdk@sha256:dc9854895457f57b97ba64696754ec06cce4cb51435bb0a8a304f7988d5614d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2299851 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c274be162c0c8f309fca60a27b661d3f008acb7cc76b43ed7a16e11a96382b5`

```dockerfile
```

-	Layers:
	-	`sha256:53d08d8f4cdb02a868b48fc0da0c75e5c3aa4938f96448baa5df9e5d7260226b`  
		Last Modified: Tue, 09 Sep 2025 00:23:38 GMT  
		Size: 2.3 MB (2281508 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9e11fe159e51b9d1d277d67f80ce17ee3f687a4043a808c1937bbba8e76c3015`  
		Last Modified: Tue, 09 Sep 2025 00:23:39 GMT  
		Size: 18.3 KB (18343 bytes)  
		MIME: application/vnd.in-toto+json
