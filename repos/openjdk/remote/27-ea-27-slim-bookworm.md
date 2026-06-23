## `openjdk:27-ea-27-slim-bookworm`

```console
$ docker pull openjdk@sha256:3dc4d0a91d048f226bccbeb9e346aab1e5204342ac573c09cc3b18b447fa1b3e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:27-ea-27-slim-bookworm` - linux; amd64

```console
$ docker pull openjdk@sha256:dc8e78ac39158f06367073212f30dc0971c6cf23bdea8a4913242f2445c22827
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **259.4 MB (259387273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47223f1fc763e837b80c02899c863d0b03db7fba118fee55603e7017e5ee8f3f`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1781049600'
# Mon, 22 Jun 2026 22:38:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 22 Jun 2026 22:38:31 GMT
ENV JAVA_HOME=/usr/local/openjdk-27
# Mon, 22 Jun 2026 22:38:31 GMT
ENV PATH=/usr/local/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jun 2026 22:38:31 GMT
ENV LANG=C.UTF-8
# Mon, 22 Jun 2026 22:38:31 GMT
ENV JAVA_VERSION=27-ea+27
# Mon, 22 Jun 2026 22:38:31 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/27/GPL/openjdk-27-ea+27_linux-x64_bin.tar.gz'; 			downloadSha256='4f81468b39b9f6516ce5e3de3130e404d508be7d77d601ec1217056163ff6a6e'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/27/GPL/openjdk-27-ea+27_linux-aarch64_bin.tar.gz'; 			downloadSha256='048e4f60c3069ab86e0a068eedd93e33e62ec275a1b2a9033bb07c925f01b7c9'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Mon, 22 Jun 2026 22:38:31 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:b9136609bef0128191aa157637b98dd7b98e52154ca60c18258d65957a01c6d0`  
		Last Modified: Wed, 10 Jun 2026 23:39:54 GMT  
		Size: 28.2 MB (28237624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e893b77ddd69a82dba8b28a6a97dacae259c4072ed4a70d9ddaa4c9ad978b05`  
		Last Modified: Mon, 22 Jun 2026 22:38:52 GMT  
		Size: 4.0 MB (4032914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ac0ab43d8f8e34929d187faa4503db1755ce60a8ca1b8c6793c6f80ec26f1b8`  
		Last Modified: Mon, 22 Jun 2026 22:38:57 GMT  
		Size: 227.1 MB (227116735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-27-slim-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:f668e9ca57f62c36f6e51ae25c1c15ba90a1c3cdaaddbd638a180a87e0661193
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2664161 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fef53891ccbd0b62ef7c8d7a5897523dcd542741969bd00d3c0664eaaecc0f2d`

```dockerfile
```

-	Layers:
	-	`sha256:6924399d9be12c17df65404be5b97dc8bc5a311dd4a045ab79387c2344eabe09`  
		Last Modified: Mon, 22 Jun 2026 22:38:52 GMT  
		Size: 2.6 MB (2647290 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1a45bc1098f24da83c2d496b92121e4ffe8f8db2e121e32536d3db1cd7f5500e`  
		Last Modified: Mon, 22 Jun 2026 22:38:51 GMT  
		Size: 16.9 KB (16871 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:27-ea-27-slim-bookworm` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:b19704b3b081ce8dae755debd743c6538cfbd477ae4ce7c3c3f62f3409c9d6d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.1 MB (257074339 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:add1fd46d3e9fcdab0c7ed1b9e25e796ef9addefc9ebc27fb6c9dc046bde28bb`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1781049600'
# Mon, 22 Jun 2026 22:37:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 22 Jun 2026 22:38:06 GMT
ENV JAVA_HOME=/usr/local/openjdk-27
# Mon, 22 Jun 2026 22:38:06 GMT
ENV PATH=/usr/local/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jun 2026 22:38:06 GMT
ENV LANG=C.UTF-8
# Mon, 22 Jun 2026 22:38:06 GMT
ENV JAVA_VERSION=27-ea+27
# Mon, 22 Jun 2026 22:38:06 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/27/GPL/openjdk-27-ea+27_linux-x64_bin.tar.gz'; 			downloadSha256='4f81468b39b9f6516ce5e3de3130e404d508be7d77d601ec1217056163ff6a6e'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/27/GPL/openjdk-27-ea+27_linux-aarch64_bin.tar.gz'; 			downloadSha256='048e4f60c3069ab86e0a068eedd93e33e62ec275a1b2a9033bb07c925f01b7c9'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Mon, 22 Jun 2026 22:38:06 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:402614bd39aaec1e4bdcf25aa67f88588fc8d93997a2551c4e130e6ed2b06c7a`  
		Last Modified: Wed, 10 Jun 2026 23:39:57 GMT  
		Size: 28.1 MB (28122307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b8e0a859591991e465c4db7aec5cdc618b20a2aac6ec06fda6a1fc12d1588f0`  
		Last Modified: Mon, 22 Jun 2026 22:38:27 GMT  
		Size: 3.9 MB (3852914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd3b17f22f655006c2125e9bd084d208826592d91d289b2ba579b381e3e1d272`  
		Last Modified: Mon, 22 Jun 2026 22:38:32 GMT  
		Size: 225.1 MB (225099118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-27-slim-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:41e7d67b9d7f69d57aa97a078ef76ab84e37b40dd03d174b56913ccc29b457a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2663914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:931c6353ea808e0177351356975973a22b68b23a784ad93f58c7bcc35bafb4ab`

```dockerfile
```

-	Layers:
	-	`sha256:ff48dbff87de01b189758ef562775bf8709029cab8b41b8790fda72a3823f88b`  
		Last Modified: Mon, 22 Jun 2026 22:38:27 GMT  
		Size: 2.6 MB (2646924 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a1fb1a3e48beda98ab9bbf24db009549be2a8e67298cecf31b1f920ffc15a28e`  
		Last Modified: Mon, 22 Jun 2026 22:38:27 GMT  
		Size: 17.0 KB (16990 bytes)  
		MIME: application/vnd.in-toto+json
