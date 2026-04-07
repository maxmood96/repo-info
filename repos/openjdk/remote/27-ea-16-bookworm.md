## `openjdk:27-ea-16-bookworm`

```console
$ docker pull openjdk@sha256:281a6762756eda61047118d005d124303bb02bbb55e2931ff89f01ab82dc68c5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:27-ea-16-bookworm` - linux; amd64

```console
$ docker pull openjdk@sha256:d91d6524b78175d038d3511be6f0de03c99bb2bb76cf1395cd87b2b9f1057ad8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **382.8 MB (382775703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d83850305e57862de4608880e5a852c96abcd7e01b593250e400d08a6b3eb6ca`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 01:46:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:42:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 03:24:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 03:25:00 GMT
ENV JAVA_HOME=/usr/local/openjdk-27
# Tue, 07 Apr 2026 03:25:00 GMT
ENV PATH=/usr/local/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 03:25:00 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 03:25:00 GMT
ENV JAVA_VERSION=27-ea+16
# Tue, 07 Apr 2026 03:25:00 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/16/GPL/openjdk-27-ea+16_linux-x64_bin.tar.gz'; 			downloadSha256='a9c8f46b87d1c973c4749728845de23d38a1897dc78b85e362f76ce98ca826eb'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/16/GPL/openjdk-27-ea+16_linux-aarch64_bin.tar.gz'; 			downloadSha256='cc96a894335065d7218341881222321567d1eca6950b3d6433fc387295d8d3b0'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 07 Apr 2026 03:25:00 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:c150dd3f5fc91eabd1818cc30298a4a956782621583cadfd369c4d327584008e`  
		Last Modified: Tue, 07 Apr 2026 00:10:26 GMT  
		Size: 48.5 MB (48488823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2c3414b1d6b49c54c305584faac46aad75c67644cf4f8495e8145206d28e416`  
		Last Modified: Tue, 07 Apr 2026 01:47:02 GMT  
		Size: 24.0 MB (24038269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de73ef470b7b271fede6f98a4c8376971bd059ce04ebc13b9f86e34e534b89ae`  
		Last Modified: Tue, 07 Apr 2026 02:43:01 GMT  
		Size: 64.4 MB (64396012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:114e8fcc9c8b27ef332948e3a50a00ed5e9bcd85616c310c50cc8af06e293226`  
		Last Modified: Tue, 07 Apr 2026 03:25:30 GMT  
		Size: 16.9 MB (16945640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:160adee9fe213b6ea3f099d02b032f2811b1e6018e7c01afbdc179948c9dca6f`  
		Last Modified: Tue, 07 Apr 2026 03:25:34 GMT  
		Size: 228.9 MB (228906959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-16-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:dd740519b6549ff311555f8adcd7af0a01faab02c5c5057ab28e495c3bf1cef2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 MB (8686826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b289bf02a52633ef485ee6d598ad02f07dcade088f1b9bce9fd44eeb6cd86ee`

```dockerfile
```

-	Layers:
	-	`sha256:eb48063adf54b8b652171a714bc0a67dcbafb51d34dedcfd6c2866f64a665bd9`  
		Last Modified: Tue, 07 Apr 2026 03:25:30 GMT  
		Size: 8.7 MB (8668887 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8916476543d7d7de63781522c492ef73c6c0698a44d1013adf0ef0e0a4b01636`  
		Last Modified: Tue, 07 Apr 2026 03:25:29 GMT  
		Size: 17.9 KB (17939 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:27-ea-16-bookworm` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:8e43ae728e3b223b3f02cd229905dcf28f577068b97a21df314eeac40f1f6335
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **381.1 MB (381057417 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:795593a8c2b4b0ad814dfe702f79fc4f0850bccef5b2691994d38a87dbc0a20f`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 01:49:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:52:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 03:36:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 03:36:58 GMT
ENV JAVA_HOME=/usr/local/openjdk-27
# Tue, 07 Apr 2026 03:36:58 GMT
ENV PATH=/usr/local/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 03:36:58 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 03:36:58 GMT
ENV JAVA_VERSION=27-ea+16
# Tue, 07 Apr 2026 03:36:58 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/16/GPL/openjdk-27-ea+16_linux-x64_bin.tar.gz'; 			downloadSha256='a9c8f46b87d1c973c4749728845de23d38a1897dc78b85e362f76ce98ca826eb'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/16/GPL/openjdk-27-ea+16_linux-aarch64_bin.tar.gz'; 			downloadSha256='cc96a894335065d7218341881222321567d1eca6950b3d6433fc387295d8d3b0'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 07 Apr 2026 03:36:58 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:d03e31a3f7ef0d2866d799846c3a18286fab6fcddbd8c523f3cb5ed1bd2f31a3`  
		Last Modified: Tue, 07 Apr 2026 00:10:26 GMT  
		Size: 48.4 MB (48373262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0af98f0879b367460715b477e9118922ba24f17d9a4ad8d70e595a9c4cf56990`  
		Last Modified: Tue, 07 Apr 2026 01:49:50 GMT  
		Size: 23.6 MB (23604705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95b913dee6e116304b9bb2391ef8aedbb1f5ee16d167338920c7609a48bdd772`  
		Last Modified: Tue, 07 Apr 2026 02:53:06 GMT  
		Size: 64.5 MB (64479508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:297e5f47fcc1de6cb721c86bf9793f7bcde7ba2cca5f48a9a3206d22c69d4c32`  
		Last Modified: Tue, 07 Apr 2026 03:37:26 GMT  
		Size: 17.7 MB (17729148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b01bf6f22be9306fd55edae39302443309ad902e637085596338591e52a02c8`  
		Last Modified: Tue, 07 Apr 2026 03:37:30 GMT  
		Size: 226.9 MB (226870794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-16-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:3e1b910398d34531c068be335113cceff7a323c6652ddbf3c304434ad3619516
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8823790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f0daec5c9f27d099a31da757cb92aa37e2ac31424b25b6d26dfe05559f7a4f1`

```dockerfile
```

-	Layers:
	-	`sha256:bfc7b4ce1827ca871ba7e908db936ab5df8256520d61f3e361596404dcf0c765`  
		Last Modified: Tue, 07 Apr 2026 03:37:25 GMT  
		Size: 8.8 MB (8805732 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2aeafad80d419b922cea30e4e7ac285943a5c97bd65bccefcfc537bfef68f399`  
		Last Modified: Tue, 07 Apr 2026 03:37:25 GMT  
		Size: 18.1 KB (18058 bytes)  
		MIME: application/vnd.in-toto+json
