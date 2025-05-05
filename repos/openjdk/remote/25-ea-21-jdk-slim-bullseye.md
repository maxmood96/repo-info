## `openjdk:25-ea-21-jdk-slim-bullseye`

```console
$ docker pull openjdk@sha256:a920b98eaa540ed06e1c766966b0ba8a41c6a8c935b695da79e539a05d0c118d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `openjdk:25-ea-21-jdk-slim-bullseye` - linux; amd64

```console
$ docker pull openjdk@sha256:2f746c6919ad8a8687707e60c364504868b2cb10fc0120b67dff7fa51f6e27b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **245.3 MB (245283982 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56c036c007f2228cfd8e1e39515e2bad8801220a93c569041663ad7b7217d68e`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1745798400'
# Sat, 03 May 2025 00:48:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 03 May 2025 00:48:11 GMT
ENV JAVA_HOME=/usr/local/openjdk-25
# Sat, 03 May 2025 00:48:11 GMT
ENV PATH=/usr/local/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 03 May 2025 00:48:11 GMT
ENV LANG=C.UTF-8
# Sat, 03 May 2025 00:48:11 GMT
ENV JAVA_VERSION=25-ea+21
# Sat, 03 May 2025 00:48:11 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/21/GPL/openjdk-25-ea+21_linux-x64_bin.tar.gz'; 			downloadSha256='9215df470d2d44c8ea731dcde9e170b6951e29f6e96e90625be983f0f9cfd1ef'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/21/GPL/openjdk-25-ea+21_linux-aarch64_bin.tar.gz'; 			downloadSha256='23b6cbdac4dedcb1e7d290e7f5e9da01be8c4dcc35b4d296054aae3588d4465a'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 03 May 2025 00:48:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:c8e1eb8ab3b017bd9e33ddec83ebdd8292c542bbd14a8d5a6cfa2edc3ad3b8eb`  
		Last Modified: Mon, 28 Apr 2025 21:08:07 GMT  
		Size: 30.3 MB (30254604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fb4b00f264added788f8fc79e339acdd71ca6a679fcd303fe6172487abae64d`  
		Last Modified: Mon, 05 May 2025 17:30:12 GMT  
		Size: 1.6 MB (1581792 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8609ba55db3467a24a2d50af9ea40b9941a373a635ff15be3803ace120f226ae`  
		Last Modified: Mon, 05 May 2025 17:30:17 GMT  
		Size: 213.4 MB (213447586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-ea-21-jdk-slim-bullseye` - unknown; unknown

```console
$ docker pull openjdk@sha256:aae7e4736088a1578c964f8ae205253a617e7278250213e26c9cd9fcfb43c8bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2846831 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e8c2e61f4702afee96c4d2c2b367ad63f4346d72ecfad35640313c4fc2a86db`

```dockerfile
```

-	Layers:
	-	`sha256:dfdefc63aae994b5d79307b6591df66ae7a0eca023f70765307b4dabf2e2c710`  
		Last Modified: Mon, 05 May 2025 17:30:12 GMT  
		Size: 2.8 MB (2829261 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8164ce76467fae02cf1254c1059293c8ccc3b571b0f7190d9461a37564d3a4bf`  
		Last Modified: Mon, 05 May 2025 17:30:12 GMT  
		Size: 17.6 KB (17570 bytes)  
		MIME: application/vnd.in-toto+json
