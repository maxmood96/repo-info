## `openjdk:25-ea-10-jdk-slim`

```console
$ docker pull openjdk@sha256:057667ae67c2d6df51320fec3dbb11c8764ede7f845f9b1325cdc74de627ce5c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:25-ea-10-jdk-slim` - linux; amd64

```console
$ docker pull openjdk@sha256:543a6f498255557baaa9ee4e3479f6c4fe6404f202430bd0069d33a2dd559f93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.2 MB (244248287 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8edd61dfddf9e706e9bdaf0d864db4c6c4dd8b5a209f3cbe9fee165a079e1293`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 03 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1738540800'
# Fri, 14 Feb 2025 19:48:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Feb 2025 19:48:17 GMT
ENV JAVA_HOME=/usr/local/openjdk-25
# Fri, 14 Feb 2025 19:48:17 GMT
ENV PATH=/usr/local/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 14 Feb 2025 19:48:17 GMT
ENV LANG=C.UTF-8
# Fri, 14 Feb 2025 19:48:17 GMT
ENV JAVA_VERSION=25-ea+10
# Fri, 14 Feb 2025 19:48:17 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/10/GPL/openjdk-25-ea+10_linux-x64_bin.tar.gz'; 			downloadSha256='e9104a397a3c30011ed27d8c6bf111870ec59b10e1af8f028ea526c7743d07d0'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/10/GPL/openjdk-25-ea+10_linux-aarch64_bin.tar.gz'; 			downloadSha256='043e5bc3eba8fc6c21815fd310f205cfc481911219ee95faa5b2185dc375f6eb'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 14 Feb 2025 19:48:17 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:c29f5b76f736a8b555fd191c48d6581bb918bcd605a7cbcc76205dd6acff3260`  
		Last Modified: Tue, 04 Feb 2025 04:27:59 GMT  
		Size: 28.2 MB (28212303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ec6f123d65ece5e8580442159e109cdbdfa19c8e99e1c95237a6871ff6cc7a4`  
		Last Modified: Sat, 15 Feb 2025 01:36:10 GMT  
		Size: 4.0 MB (4018393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cb33873854c92fec66daaf78316d0d57de7cdb008b685cac91ba0604a385ee7`  
		Last Modified: Sat, 15 Feb 2025 01:36:16 GMT  
		Size: 212.0 MB (212017591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-ea-10-jdk-slim` - unknown; unknown

```console
$ docker pull openjdk@sha256:c4f4d9ecc073abf0072f354070ac15aee82ba7954d2579aedabdfbfc6ba5db74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2557092 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e7993ec895bce7106a368d8a7526d6d169b242b0691b447f9d9f53ab15e0f8c`

```dockerfile
```

-	Layers:
	-	`sha256:1a51e639d8b6d89dd8c3679e48daa9dd8c4736a7082fa1426ce491ce5deed68d`  
		Last Modified: Sat, 15 Feb 2025 01:24:32 GMT  
		Size: 2.5 MB (2537650 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8d2fd1cd34adc8560f13bcc54d88b3bebdf1c832a285332a180f5258e2225d32`  
		Last Modified: Sat, 15 Feb 2025 01:24:32 GMT  
		Size: 19.4 KB (19442 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:25-ea-10-jdk-slim` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:bf6acf2c64c6256693d9115d03dffcc4935f96774f0fa3443c9acc9f29bc01ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.8 MB (241835518 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f192b84158433ad60c146366de0e6f3591eba8164e4a880efbaba43801547da7`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 03 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1738540800'
# Fri, 14 Feb 2025 19:48:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Feb 2025 19:48:17 GMT
ENV JAVA_HOME=/usr/local/openjdk-25
# Fri, 14 Feb 2025 19:48:17 GMT
ENV PATH=/usr/local/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 14 Feb 2025 19:48:17 GMT
ENV LANG=C.UTF-8
# Fri, 14 Feb 2025 19:48:17 GMT
ENV JAVA_VERSION=25-ea+10
# Fri, 14 Feb 2025 19:48:17 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/10/GPL/openjdk-25-ea+10_linux-x64_bin.tar.gz'; 			downloadSha256='e9104a397a3c30011ed27d8c6bf111870ec59b10e1af8f028ea526c7743d07d0'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/10/GPL/openjdk-25-ea+10_linux-aarch64_bin.tar.gz'; 			downloadSha256='043e5bc3eba8fc6c21815fd310f205cfc481911219ee95faa5b2185dc375f6eb'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 14 Feb 2025 19:48:17 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:4d2547c084994a809c138e688fbe4ee14eedbc6e2defc5b1c680edd16e291473`  
		Last Modified: Tue, 04 Feb 2025 04:29:51 GMT  
		Size: 28.0 MB (28040881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d43b4f96d2c0ec3b3b9b795e151e48b648a3451851e1ceb16e34f7cb4fbebe83`  
		Last Modified: Wed, 05 Feb 2025 06:59:29 GMT  
		Size: 3.8 MB (3833699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f53c90bddac87f75071524b84a074a3a3f615ef266a98125d551f900252c13f`  
		Last Modified: Sat, 15 Feb 2025 08:51:55 GMT  
		Size: 210.0 MB (209960938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-ea-10-jdk-slim` - unknown; unknown

```console
$ docker pull openjdk@sha256:8c7f97902e003fb8d3e232dcbe25c00f4f9f26ac41fa79a70e14c0793c28b94c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2557036 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e40a09c5a1b46f977488f4f38f20f62e2fc4f2e4729853fbfbe71cb8476e8146`

```dockerfile
```

-	Layers:
	-	`sha256:96704745fcc2d7ddf29609f42b7a69f1a57f437b4992926fd50025fda6bdfb61`  
		Last Modified: Sat, 15 Feb 2025 10:24:00 GMT  
		Size: 2.5 MB (2537380 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d3d02d47fbc3c2a98565eb107b49873405101148d7ab181360cb2128b175ff09`  
		Last Modified: Sat, 15 Feb 2025 10:24:00 GMT  
		Size: 19.7 KB (19656 bytes)  
		MIME: application/vnd.in-toto+json
