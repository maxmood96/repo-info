## `openjdk:26-ea-jdk-slim-trixie`

```console
$ docker pull openjdk@sha256:0ab1f3d78abe21794d63a103ab7f9dd690725345da0d658b0be783bd77904331
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:26-ea-jdk-slim-trixie` - linux; amd64

```console
$ docker pull openjdk@sha256:6c77e370435f68edc5e13caba766298263dac6270821a7f6b6cce47384c18f20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **260.2 MB (260161832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad42997e43108a0aebf25141d2c33584d4ce68406a77e32ddc31bb3cb14e7f55`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1766966400'
# Mon, 12 Jan 2026 20:07:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 12 Jan 2026 20:07:43 GMT
ENV JAVA_HOME=/usr/local/openjdk-26
# Mon, 12 Jan 2026 20:07:43 GMT
ENV PATH=/usr/local/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 12 Jan 2026 20:07:43 GMT
ENV LANG=C.UTF-8
# Mon, 12 Jan 2026 20:07:43 GMT
ENV JAVA_VERSION=26-ea+30
# Mon, 12 Jan 2026 20:07:43 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/30/GPL/openjdk-26-ea+30_linux-x64_bin.tar.gz'; 			downloadSha256='300f7c67876f470e3ddacfd75be07c3c92812847b43933eb3600e258a9662e2d'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/30/GPL/openjdk-26-ea+30_linux-aarch64_bin.tar.gz'; 			downloadSha256='466961f9222d91364dbc631bb8c76216dbecaf025464f0189b3acc96dd516a96'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Mon, 12 Jan 2026 20:07:43 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:02d7611c4eae219af91448a4720bdba036575d3bc0356cfe12774af85daa6aff`  
		Last Modified: Mon, 29 Dec 2025 22:31:18 GMT  
		Size: 29.8 MB (29776533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af54f42b2f1fd285aeeb515e03caf67d7f5c017e51501a9b917a1e473fc65f37`  
		Last Modified: Mon, 12 Jan 2026 20:08:15 GMT  
		Size: 2.4 MB (2371013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62e2abf543b015d0e566a2cb9a90d29ae28f3815996d2c0489b7308f972a221c`  
		Last Modified: Mon, 12 Jan 2026 20:08:26 GMT  
		Size: 228.0 MB (228014286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-ea-jdk-slim-trixie` - unknown; unknown

```console
$ docker pull openjdk@sha256:a2e2202bae68a37f943c3cb1341be55c0a5db61ea0e986a4eba92843d47788cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2296898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c462dce829e311211355d70c8ca3ac10086400dd4977a4680bb0edb3822f2de`

```dockerfile
```

-	Layers:
	-	`sha256:551c0a058ac44c96ed423c20369610c4ca39208943df9b6fa1f0f3d195dacde4`  
		Last Modified: Mon, 12 Jan 2026 22:24:12 GMT  
		Size: 2.3 MB (2278789 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:86995456c065967c0d7ba6dbd86842060d818148ac94f3511b70a46efa6bf95a`  
		Last Modified: Mon, 12 Jan 2026 22:24:13 GMT  
		Size: 18.1 KB (18109 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:26-ea-jdk-slim-trixie` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:2df5aee1e5e13464eaba5206baa81c507c01ada3a8a0bb1bcf7aa327705f3fc2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.4 MB (258386063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d451ed086ccc73ef23031e3fefedc568fdb2379175b2396ac17fcbe8150d0279`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1766966400'
# Mon, 12 Jan 2026 20:08:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 12 Jan 2026 20:08:31 GMT
ENV JAVA_HOME=/usr/local/openjdk-26
# Mon, 12 Jan 2026 20:08:31 GMT
ENV PATH=/usr/local/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 12 Jan 2026 20:08:31 GMT
ENV LANG=C.UTF-8
# Mon, 12 Jan 2026 20:08:31 GMT
ENV JAVA_VERSION=26-ea+30
# Mon, 12 Jan 2026 20:08:31 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/30/GPL/openjdk-26-ea+30_linux-x64_bin.tar.gz'; 			downloadSha256='300f7c67876f470e3ddacfd75be07c3c92812847b43933eb3600e258a9662e2d'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/30/GPL/openjdk-26-ea+30_linux-aarch64_bin.tar.gz'; 			downloadSha256='466961f9222d91364dbc631bb8c76216dbecaf025464f0189b3acc96dd516a96'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Mon, 12 Jan 2026 20:08:31 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2ae15a20160209c6fd6cff4886e4ba2e666fa5bedd7b54a2c0097ea6646f0273`  
		Last Modified: Mon, 29 Dec 2025 22:31:09 GMT  
		Size: 30.1 MB (30138636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2139e9bc3c188c80bdfa24fd207be28056b7591868d025adc113b88a53c57f9c`  
		Last Modified: Mon, 12 Jan 2026 20:09:07 GMT  
		Size: 2.3 MB (2314136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a108f111157bfbab9e7518e3f384b7d678f1b45c16412bc729212ecd1aa7f89a`  
		Last Modified: Mon, 12 Jan 2026 20:09:13 GMT  
		Size: 225.9 MB (225933291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-ea-jdk-slim-trixie` - unknown; unknown

```console
$ docker pull openjdk@sha256:50e8597724409ab1011910cd8549dfe71d034671ff185f808da9ca790a15fc79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2296749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:467c9a8fdcbe48833a491bc6cfc40d6097f41f36f60fbfdad11de963414c5383`

```dockerfile
```

-	Layers:
	-	`sha256:bdc71984a2e09b5d34726336036ecf8f0a2a747273a412234b4ae516c2f5b46c`  
		Last Modified: Mon, 12 Jan 2026 22:24:17 GMT  
		Size: 2.3 MB (2278475 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2fa1081a1f27a6cf8daa63370c820edbd7ad30d259ff35f9b973dcce70f17e99`  
		Last Modified: Mon, 12 Jan 2026 22:24:18 GMT  
		Size: 18.3 KB (18274 bytes)  
		MIME: application/vnd.in-toto+json
