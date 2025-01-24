## `openjdk:24-jdk-slim-bookworm`

```console
$ docker pull openjdk@sha256:d2e6fa360a6fb3c7a5ff4d87e6d0f7f49bcfa6bd072fff192fe9e43c71f01d62
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:24-jdk-slim-bookworm` - linux; amd64

```console
$ docker pull openjdk@sha256:40164ac25fc37a80bc3ffa0bd5a6dbfd0852b397f76f3f58082df2c7bf49e82c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **245.2 MB (245175969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:232f58c8de9efe0581bce8059c3f9fb7ab51c3981bd9f3ea5ba92157b51f0b2c`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1736726400'
# Thu, 23 Jan 2025 19:48:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 23 Jan 2025 19:48:14 GMT
ENV JAVA_HOME=/usr/local/openjdk-24
# Thu, 23 Jan 2025 19:48:14 GMT
ENV PATH=/usr/local/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Jan 2025 19:48:14 GMT
ENV LANG=C.UTF-8
# Thu, 23 Jan 2025 19:48:14 GMT
ENV JAVA_VERSION=24-ea+32
# Thu, 23 Jan 2025 19:48:14 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/32/GPL/openjdk-24-ea+32_linux-x64_bin.tar.gz'; 			downloadSha256='52afbfd5229250d1a724367cda6380f2acff08c58ee9bfcc6db727ccf4feb251'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/32/GPL/openjdk-24-ea+32_linux-aarch64_bin.tar.gz'; 			downloadSha256='4c6890d8da82bc38820c3b8330579c9083a6dbc834c5026def54e9b83bc18dbe'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Thu, 23 Jan 2025 19:48:14 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:af302e5c37e9dc1dbe2eadc8f5059d82a914066b541b0d1a6daa91d0cc55057d`  
		Last Modified: Tue, 14 Jan 2025 01:33:13 GMT  
		Size: 28.2 MB (28212417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49b8a1dced756a72669f4d6b5366c356485c7811a7240d212ab044c2d5797687`  
		Last Modified: Thu, 23 Jan 2025 22:26:33 GMT  
		Size: 4.0 MB (4018402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afb410f0c4ff654c175db62b30288b431ccad2ab65498e95519b23d6ba7711e5`  
		Last Modified: Thu, 23 Jan 2025 22:26:37 GMT  
		Size: 212.9 MB (212945150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-jdk-slim-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:84b69bad479ad7ca3d04a05466c1a20bf5ea305bf578fe4439c49f252c920c54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2553961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db9f24a235b42e8bdc01cda05cc8e301c4bdfae65ce4110db31f83bf54649899`

```dockerfile
```

-	Layers:
	-	`sha256:abe7a81c5dc1bf56795812aa0739dcb540f8e9e2a6ed0407ef938257d14bf98b`  
		Last Modified: Thu, 23 Jan 2025 22:26:33 GMT  
		Size: 2.5 MB (2534519 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a190fb1fcf319fdb015a4a0ed33dad8cd5323ae33a1f5c76e85c31868d4444e6`  
		Last Modified: Thu, 23 Jan 2025 22:26:34 GMT  
		Size: 19.4 KB (19442 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:24-jdk-slim-bookworm` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:4b6f48339055eb53a4e1c861151d4b29d8bbff8d5040268497e02efc7f8961b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.8 MB (242772880 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0554d7e42a4925d165fae94685567d2320f5b276468f1005f9b0d10ebd10cb75`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1736726400'
# Thu, 23 Jan 2025 19:48:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 23 Jan 2025 19:48:14 GMT
ENV JAVA_HOME=/usr/local/openjdk-24
# Thu, 23 Jan 2025 19:48:14 GMT
ENV PATH=/usr/local/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Jan 2025 19:48:14 GMT
ENV LANG=C.UTF-8
# Thu, 23 Jan 2025 19:48:14 GMT
ENV JAVA_VERSION=24-ea+32
# Thu, 23 Jan 2025 19:48:14 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/32/GPL/openjdk-24-ea+32_linux-x64_bin.tar.gz'; 			downloadSha256='52afbfd5229250d1a724367cda6380f2acff08c58ee9bfcc6db727ccf4feb251'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/32/GPL/openjdk-24-ea+32_linux-aarch64_bin.tar.gz'; 			downloadSha256='4c6890d8da82bc38820c3b8330579c9083a6dbc834c5026def54e9b83bc18dbe'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Thu, 23 Jan 2025 19:48:14 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:7ce705000c390df8b2edde0e8b9c65a6677da4503a8f8fd89b355a3f827a275f`  
		Last Modified: Tue, 14 Jan 2025 01:35:55 GMT  
		Size: 28.0 MB (28041031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f083f07e13bd63cd44a785caf631d4e023799e01a18898c1a673879d76b06aa`  
		Last Modified: Wed, 22 Jan 2025 02:34:57 GMT  
		Size: 3.8 MB (3833715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0528d107681081844024b948f00df5cc6a1cd03e89dc736e108bdd95f79c15a`  
		Last Modified: Thu, 23 Jan 2025 22:36:02 GMT  
		Size: 210.9 MB (210898134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-jdk-slim-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:41dca77987c4f1d45ca99d0982cbdc31d64df1c3629cfab48bc3ae29a08835f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2553906 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4191bed7446357f495e04c30aa8bb109a6ef31660c6dcfd5d1098b99e9f05411`

```dockerfile
```

-	Layers:
	-	`sha256:6a79aae4dac463c376fb87bd2a7c439c023ae52447c76d23eb840a906a1b8f75`  
		Last Modified: Thu, 23 Jan 2025 22:35:58 GMT  
		Size: 2.5 MB (2534249 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:affcaa47ff4e4a4fe992a3287b902a346e82d8d357cc098182390d786e3e8269`  
		Last Modified: Thu, 23 Jan 2025 22:35:57 GMT  
		Size: 19.7 KB (19657 bytes)  
		MIME: application/vnd.in-toto+json
