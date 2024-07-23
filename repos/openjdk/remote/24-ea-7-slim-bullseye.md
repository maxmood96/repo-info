## `openjdk:24-ea-7-slim-bullseye`

```console
$ docker pull openjdk@sha256:c1d6ef772cf8000de7967b3a925a3086ffdeabbe71cbec1ebe0d8e5e348efd1a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `openjdk:24-ea-7-slim-bullseye` - linux; amd64

```console
$ docker pull openjdk@sha256:a27b6ac87003fb4340a493d2a67ef73c5da685208a1e55fc31045ac57e9452ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.7 MB (244694417 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58e7d0b990d22e0fdd57280c09e1381082086a9990607b74b19ce923b1a13107`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 02 Jul 2024 01:25:24 GMT
ADD file:49759b7a74bac875e3619e20ed5a9521101c7729f601d90976d0755d30e97499 in / 
# Tue, 02 Jul 2024 01:25:24 GMT
CMD ["bash"]
# Sat, 20 Jul 2024 00:52:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 20 Jul 2024 00:52:05 GMT
ENV JAVA_HOME=/usr/local/openjdk-24
# Sat, 20 Jul 2024 00:52:05 GMT
ENV PATH=/usr/local/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 20 Jul 2024 00:52:05 GMT
ENV LANG=C.UTF-8
# Sat, 20 Jul 2024 00:52:05 GMT
ENV JAVA_VERSION=24-ea+7
# Sat, 20 Jul 2024 00:52:05 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/7/GPL/openjdk-24-ea+7_linux-x64_bin.tar.gz'; 			downloadSha256='d175c4cfc7ab8306b42cf88fe0e60b2b827a2106c026ae6d2a3f2e51bbcb60d0'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/7/GPL/openjdk-24-ea+7_linux-aarch64_bin.tar.gz'; 			downloadSha256='5df46f7b64a38a7a34e1b283f6c37b57f8238567b81c3db0f127f348f4842977'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 20 Jul 2024 00:52:05 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:76956b537f14770ffd78afbe4f17016b2794c4b9b568325e8079089ea5c4e8cd`  
		Last Modified: Tue, 02 Jul 2024 01:29:27 GMT  
		Size: 31.4 MB (31422284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae6aa98283038fd57cb3e0c854871d15982d793b38a8e43083a0d404726b36be`  
		Last Modified: Mon, 22 Jul 2024 21:00:08 GMT  
		Size: 1.6 MB (1581820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97abc78a290bb5d6cc194bb7e95c6ebdfa91cb516fcdf027b69775d2f5eaf65f`  
		Last Modified: Mon, 22 Jul 2024 21:00:14 GMT  
		Size: 211.7 MB (211690313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-ea-7-slim-bullseye` - unknown; unknown

```console
$ docker pull openjdk@sha256:a5d550fd17f71faf9d4eefcf3b6f34f0aabda54e33cdb6cfeb62c851891a7289
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2676511 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96016713f29d4f9579b273b548981331eab946c643d192e93cc3ae5ab1421333`

```dockerfile
```

-	Layers:
	-	`sha256:fa29f128d3ad42c62e7f2e21995ad916fd9f67e1af18fe562dcf174465e6ceb9`  
		Last Modified: Mon, 22 Jul 2024 21:00:08 GMT  
		Size: 2.7 MB (2659166 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:667a65ac023e3097ebaf7d7c1c3c681141d26826ec6aca889b07b529a827e28d`  
		Last Modified: Mon, 22 Jul 2024 21:00:08 GMT  
		Size: 17.3 KB (17345 bytes)  
		MIME: application/vnd.in-toto+json
