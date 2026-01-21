## `openjdk:27-ea-5-slim-trixie`

```console
$ docker pull openjdk@sha256:6934b2d4b6a6147b63a53010d9216fc925093a0881316634504a24dce4089aa8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:27-ea-5-slim-trixie` - linux; amd64

```console
$ docker pull openjdk@sha256:4d6756da8834084b258b652b5dc08a5c97e39bcc4fdacc25c67438d5912440b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **260.4 MB (260379983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bca52950ebecf892af164e373fa2ec52560a7ae8e00a81af2d29e6a12809b81`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1768176000'
# Tue, 20 Jan 2026 18:47:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 20 Jan 2026 18:47:34 GMT
ENV JAVA_HOME=/usr/local/openjdk-27
# Tue, 20 Jan 2026 18:47:34 GMT
ENV PATH=/usr/local/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 20 Jan 2026 18:47:34 GMT
ENV LANG=C.UTF-8
# Tue, 20 Jan 2026 18:47:34 GMT
ENV JAVA_VERSION=27-ea+5
# Tue, 20 Jan 2026 18:47:34 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/5/GPL/openjdk-27-ea+5_linux-x64_bin.tar.gz'; 			downloadSha256='2d85f5a6432abd2eb67b974ed1ab85d2a9557b06be285f2fc6e5d94429951468'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/5/GPL/openjdk-27-ea+5_linux-aarch64_bin.tar.gz'; 			downloadSha256='58f4450fff4f277000cf3d520a612275b0d9b6cb24e1287457d4651e98714b4a'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 20 Jan 2026 18:47:34 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:119d43eec815e5f9a47da3a7d59454581b1e204b0c34db86f171b7ceb3336533`  
		Last Modified: Tue, 13 Jan 2026 00:42:34 GMT  
		Size: 29.8 MB (29773685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db62493ed6c8a4aaff129f945aed0cf864b114b8d07ebecba430b369fe7b7547`  
		Last Modified: Tue, 20 Jan 2026 18:48:03 GMT  
		Size: 2.4 MB (2371079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b3ae285470cb40527617cf141b11c861548af5211b8c054ae30f674f7fc3467`  
		Last Modified: Tue, 20 Jan 2026 18:47:58 GMT  
		Size: 228.2 MB (228235219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-5-slim-trixie` - unknown; unknown

```console
$ docker pull openjdk@sha256:970833621440bc3eb0d430c66b4104dd58863f43c242842c36494d4fc3768d79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2296927 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d99cc1e41e425bbac633d7cbd6d48677747aec62a6ad50247212a35d0921603`

```dockerfile
```

-	Layers:
	-	`sha256:b9f1c05e1c85dca1c26fc456d68c13575748fa7cdd4221ea496cd9ed0fba3d6c`  
		Last Modified: Tue, 20 Jan 2026 18:47:53 GMT  
		Size: 2.3 MB (2278839 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:42800e695a23ae3a7b9cd942e3001d744e0a4b555e01883e052c847bcfce478a`  
		Last Modified: Tue, 20 Jan 2026 18:47:53 GMT  
		Size: 18.1 KB (18088 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:27-ea-5-slim-trixie` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:25be7e9b6bde11cb49b37c01ee6add18aa77a068120b1052bd2018d6b6b86b6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.6 MB (258618091 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83d0b32064a3d464559e2375ca7a7ba58a5a3e56a81268daa65df7dabb0473b7`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1768176000'
# Tue, 20 Jan 2026 18:47:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 20 Jan 2026 18:48:00 GMT
ENV JAVA_HOME=/usr/local/openjdk-27
# Tue, 20 Jan 2026 18:48:00 GMT
ENV PATH=/usr/local/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 20 Jan 2026 18:48:00 GMT
ENV LANG=C.UTF-8
# Tue, 20 Jan 2026 18:48:00 GMT
ENV JAVA_VERSION=27-ea+5
# Tue, 20 Jan 2026 18:48:00 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/5/GPL/openjdk-27-ea+5_linux-x64_bin.tar.gz'; 			downloadSha256='2d85f5a6432abd2eb67b974ed1ab85d2a9557b06be285f2fc6e5d94429951468'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/5/GPL/openjdk-27-ea+5_linux-aarch64_bin.tar.gz'; 			downloadSha256='58f4450fff4f277000cf3d520a612275b0d9b6cb24e1287457d4651e98714b4a'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 20 Jan 2026 18:48:00 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:d637807aba98f742a62ad9b0146579ceb0297a3c831f56b2361664b7f5fbc75b`  
		Last Modified: Tue, 13 Jan 2026 00:42:41 GMT  
		Size: 30.1 MB (30134042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9421c17d5db480ff1158775b4a95116be19dcafb0118a171a6ca1ed112cae7c7`  
		Last Modified: Tue, 20 Jan 2026 18:48:21 GMT  
		Size: 2.3 MB (2314134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9292e4711e9be64a8956baf1af0994f9981e8a3ea3e6a4dc974ed4efaf09785`  
		Last Modified: Tue, 20 Jan 2026 18:48:27 GMT  
		Size: 226.2 MB (226169915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-5-slim-trixie` - unknown; unknown

```console
$ docker pull openjdk@sha256:be0b2f84a7eb761e57c3194d3df2c7fcc1a0dba1d0a58542c266ae92b91563df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2296780 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2eb0293a537bebee369cc79d11ae82a514eb981cf2a6a471f2f4ef5fe1ec044e`

```dockerfile
```

-	Layers:
	-	`sha256:cd0a2c7cb258caf9f1f74f9bf36f7cb9ab539c49e35e40804bd0bf9445f0f384`  
		Last Modified: Tue, 20 Jan 2026 19:26:26 GMT  
		Size: 2.3 MB (2278525 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bf4a6b294074574797ccca77cce078715c4c566dba102c805f1a021e158aad93`  
		Last Modified: Tue, 20 Jan 2026 19:26:27 GMT  
		Size: 18.3 KB (18255 bytes)  
		MIME: application/vnd.in-toto+json
