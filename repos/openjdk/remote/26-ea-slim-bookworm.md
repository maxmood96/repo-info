## `openjdk:26-ea-slim-bookworm`

```console
$ docker pull openjdk@sha256:7e6817126ef749edb0655282416bed2fe6a6535d59996b0ef901ab8930c52713
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:26-ea-slim-bookworm` - linux; amd64

```console
$ docker pull openjdk@sha256:265fa7c0b4091434edda07833d12ed7c771f01173bf0b88ed234b4bb88483398
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.2 MB (255203616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:508e0f3fad21ad8eb9adfdbbf108606b04db1ba4464a232b3ca1f371a8f370ea`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 10 Jun 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1749513600'
# Sat, 14 Jun 2025 00:54:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 14 Jun 2025 00:54:06 GMT
ENV JAVA_HOME=/usr/local/openjdk-26
# Sat, 14 Jun 2025 00:54:06 GMT
ENV PATH=/usr/local/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 14 Jun 2025 00:54:06 GMT
ENV LANG=C.UTF-8
# Sat, 14 Jun 2025 00:54:06 GMT
ENV JAVA_VERSION=26-ea+2
# Sat, 14 Jun 2025 00:54:06 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/2/GPL/openjdk-26-ea+2_linux-x64_bin.tar.gz'; 			downloadSha256='433a629dd1072b3147cce33cf79ae06ba8c7aa9aac53f403330e8f10ec12ca76'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/2/GPL/openjdk-26-ea+2_linux-aarch64_bin.tar.gz'; 			downloadSha256='5f413ff4f8e92fcdeaf0da5315a51d2165a4017852a4a6c7e2731a8aae19e2e7'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 14 Jun 2025 00:54:06 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:dad67da3f26bce15939543965e09c4059533b025f707aad72ed3d3f3a09c66f8`  
		Last Modified: Tue, 10 Jun 2025 23:26:09 GMT  
		Size: 28.2 MB (28230129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98a06c96b83260efa4796bff08bf08f82d90d28a4c81dcaa5c1314b33c00bd40`  
		Last Modified: Mon, 16 Jun 2025 17:50:57 GMT  
		Size: 4.0 MB (4024131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e59e400d55c2ac26fa62e32022f6520042ccf2c0684bccff124704882c33b26c`  
		Last Modified: Mon, 16 Jun 2025 18:53:18 GMT  
		Size: 222.9 MB (222949356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-ea-slim-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:96ba28a6792926ee7e5c71f31d327e4152cf332893ea056395340a43011f09c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2672746 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08800120396158e759d516e8bab7445a9b98578b82c8591021b7f72d630aef58`

```dockerfile
```

-	Layers:
	-	`sha256:e076df849e931e5b7018731daa7d5440ad648ba155af371ae4708f2b6f5beb8b`  
		Last Modified: Mon, 16 Jun 2025 18:25:50 GMT  
		Size: 2.7 MB (2653321 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6a756f2a1cf1d6dc35c8c831727c68c6eeebb8c1a2556359c9463a8b61ad4a02`  
		Last Modified: Mon, 16 Jun 2025 18:25:51 GMT  
		Size: 19.4 KB (19425 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:26-ea-slim-bookworm` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:45736b7dab7b53583f98017053305f29c4fecd7f3fbf10ae4ee4b25cc822137c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **252.6 MB (252645067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf6f96ab3162a6dcbe9eed3db9665112c579ea4e679ec677fee66e6188d65c2d`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 10 Jun 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1749513600'
# Sat, 14 Jun 2025 00:54:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 14 Jun 2025 00:54:06 GMT
ENV JAVA_HOME=/usr/local/openjdk-26
# Sat, 14 Jun 2025 00:54:06 GMT
ENV PATH=/usr/local/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 14 Jun 2025 00:54:06 GMT
ENV LANG=C.UTF-8
# Sat, 14 Jun 2025 00:54:06 GMT
ENV JAVA_VERSION=26-ea+2
# Sat, 14 Jun 2025 00:54:06 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/2/GPL/openjdk-26-ea+2_linux-x64_bin.tar.gz'; 			downloadSha256='433a629dd1072b3147cce33cf79ae06ba8c7aa9aac53f403330e8f10ec12ca76'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/2/GPL/openjdk-26-ea+2_linux-aarch64_bin.tar.gz'; 			downloadSha256='5f413ff4f8e92fcdeaf0da5315a51d2165a4017852a4a6c7e2731a8aae19e2e7'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 14 Jun 2025 00:54:06 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:34ef2a75627f6089e01995bfd3b3786509bbdc7cfb4dbc804b642e195340dbc9`  
		Last Modified: Tue, 10 Jun 2025 22:48:42 GMT  
		Size: 28.1 MB (28077675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84e18990aa6eb4a8b7eff1a3a25d697c7e42c88ab4c53cdd37801790c34f6ec5`  
		Last Modified: Mon, 16 Jun 2025 17:53:12 GMT  
		Size: 3.8 MB (3836574 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60b7b933058f3269439eb4398704e5e9a7ce1f600cfbf15f2a1fb3f82210f7fb`  
		Last Modified: Mon, 16 Jun 2025 18:52:45 GMT  
		Size: 220.7 MB (220730818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-ea-slim-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:fd30f9844d2defc32bf51bfe374045f7e429a38590c3aadbb8a4f97726ae0c54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2672691 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cacf37e5dc8db5cf85b4d696a3e8a0a02550155e5958dc7c3a1f8a0b2249325c`

```dockerfile
```

-	Layers:
	-	`sha256:46f24d20857af50150cb99229e2e26b51ccef55f38b1d334daab68019eab2ed2`  
		Last Modified: Mon, 16 Jun 2025 18:25:55 GMT  
		Size: 2.7 MB (2653051 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d2d618b546ffd7e885373d5191cd3d98125a372cb46b67b30efc21a622a738b2`  
		Last Modified: Mon, 16 Jun 2025 18:25:56 GMT  
		Size: 19.6 KB (19640 bytes)  
		MIME: application/vnd.in-toto+json
