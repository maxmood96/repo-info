## `openjdk:26-ea-slim-trixie`

```console
$ docker pull openjdk@sha256:97e727960c1c96367941dc0e4ab8ba1a05bae2a60c933b5c740d7d467b4420e9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:26-ea-slim-trixie` - linux; amd64

```console
$ docker pull openjdk@sha256:1ad76cdb29ca6494c123975b9899657739f5107d396dfa04bad25654e51b0c44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.1 MB (258121560 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee35adaebf2d72cbb06bdf39c111409ff0ca9b2d3585ac572203db70f84440b1`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 20 Oct 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1760918400'
# Fri, 31 Oct 2025 20:29:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 31 Oct 2025 20:29:39 GMT
ENV JAVA_HOME=/usr/local/openjdk-26
# Fri, 31 Oct 2025 20:29:39 GMT
ENV PATH=/usr/local/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 31 Oct 2025 20:29:39 GMT
ENV LANG=C.UTF-8
# Fri, 31 Oct 2025 20:29:39 GMT
ENV JAVA_VERSION=26-ea+22
# Fri, 31 Oct 2025 20:29:39 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/22/GPL/openjdk-26-ea+22_linux-x64_bin.tar.gz'; 			downloadSha256='b87eeeb2167b024e3e62fb5ab860c0e2ad004d2e04f716b9f885d1180ac97a03'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/22/GPL/openjdk-26-ea+22_linux-aarch64_bin.tar.gz'; 			downloadSha256='b401cd0d932a4b8fd19f44deb517bfe9441097f31a2bbdb247e3b8757772e147'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 31 Oct 2025 20:29:39 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:38513bd7256313495cdd83b3b0915a633cfa475dc2a07072ab2c8d191020ca5d`  
		Last Modified: Tue, 21 Oct 2025 00:20:31 GMT  
		Size: 29.8 MB (29777924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07d81fb7b4438061d0196f8eb0e3917dabbfde6dd3be1a88af5c2662ecf31d7b`  
		Last Modified: Fri, 31 Oct 2025 20:30:13 GMT  
		Size: 2.4 MB (2371199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cba5d57c76e4d75f50eeebcc02a6e6ed3800749238c9dc5d8827fdebe43bafa`  
		Last Modified: Fri, 31 Oct 2025 21:26:08 GMT  
		Size: 226.0 MB (225972437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-ea-slim-trixie` - unknown; unknown

```console
$ docker pull openjdk@sha256:536229d3bc3b99c256453cbe7cae2f51840082da381571ecfda674978f20ab3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2300048 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:781a5dd18a3ddc2a71b5834fafa8c200ea9847024e40d496afc1f9b9f1b2c3d9`

```dockerfile
```

-	Layers:
	-	`sha256:cf02769af6ae43804851471cc9af3e1814fa9306c38ea5c562f69c98be1837c6`  
		Last Modified: Fri, 31 Oct 2025 21:24:10 GMT  
		Size: 2.3 MB (2280680 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:319d7cb8e5a8c84a1c0f7a65c6c552c91d926a912ca9ab261bcf9177f1b637aa`  
		Last Modified: Fri, 31 Oct 2025 21:24:10 GMT  
		Size: 19.4 KB (19368 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:26-ea-slim-trixie` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:f18b3e6e27edaf5977a5057077d9340c64d2bf05c9403d9464dd304938e59f5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **256.3 MB (256270213 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca29426a13395821854e7f83f37e5ad050499362298a9577310ef07643281a83`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 20 Oct 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1760918400'
# Fri, 31 Oct 2025 20:10:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 31 Oct 2025 20:10:21 GMT
ENV JAVA_HOME=/usr/local/openjdk-26
# Fri, 31 Oct 2025 20:10:21 GMT
ENV PATH=/usr/local/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 31 Oct 2025 20:10:21 GMT
ENV LANG=C.UTF-8
# Fri, 31 Oct 2025 20:10:21 GMT
ENV JAVA_VERSION=26-ea+22
# Fri, 31 Oct 2025 20:10:21 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/22/GPL/openjdk-26-ea+22_linux-x64_bin.tar.gz'; 			downloadSha256='b87eeeb2167b024e3e62fb5ab860c0e2ad004d2e04f716b9f885d1180ac97a03'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/22/GPL/openjdk-26-ea+22_linux-aarch64_bin.tar.gz'; 			downloadSha256='b401cd0d932a4b8fd19f44deb517bfe9441097f31a2bbdb247e3b8757772e147'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 31 Oct 2025 20:10:21 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:a16e551192670581ec8359c70ab9eebf8f2af5468ffc79b3d4f9ce21b0366f47`  
		Last Modified: Tue, 21 Oct 2025 00:23:17 GMT  
		Size: 30.1 MB (30142127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:845e792b32b198eeff257e877764532221b0f3a6dd7452dbf8386b166d99e9ec`  
		Last Modified: Fri, 31 Oct 2025 20:10:54 GMT  
		Size: 2.3 MB (2314260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4f70df6e82bb343a8f456a8ce2b605309867ca94956afcbceb320136c10ff40`  
		Last Modified: Fri, 31 Oct 2025 21:26:00 GMT  
		Size: 223.8 MB (223813826 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-ea-slim-trixie` - unknown; unknown

```console
$ docker pull openjdk@sha256:44523877e6ff5dba383a8aa38725a55b56f08075277736f50548d0c571804ec6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2299998 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3758584eebe6291597b3c8c45d0307332a6f863504ffef630df06bac0498f1a`

```dockerfile
```

-	Layers:
	-	`sha256:d4aec51fd627d7b8dd0203b0dd387e2879411c6d71fa8e3d52d04a26c3ac3609`  
		Last Modified: Fri, 31 Oct 2025 21:24:14 GMT  
		Size: 2.3 MB (2280414 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ab740fe66f217a3c1e8eb18fb23a88bf1a352e5c6e47d6b16acc885accd69729`  
		Last Modified: Fri, 31 Oct 2025 21:24:15 GMT  
		Size: 19.6 KB (19584 bytes)  
		MIME: application/vnd.in-toto+json
