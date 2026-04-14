## `openjdk:27-ea-slim-trixie`

```console
$ docker pull openjdk@sha256:d7745221e9598a7da6d49fc9b2197c75859281832a8f1741bba5cc463f0b78a7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:27-ea-slim-trixie` - linux; amd64

```console
$ docker pull openjdk@sha256:2bd07196d4b756c9a2d552577ffa0cf8133fc5c3b7d7f74aa1799bb4d0979696
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **264.1 MB (264129583 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b582a221165967ae6849e45fbed874716bf141eb69451ac50e14ae1691aa67bb`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1775433600'
# Tue, 14 Apr 2026 00:01:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 14 Apr 2026 00:01:18 GMT
ENV JAVA_HOME=/usr/local/openjdk-27
# Tue, 14 Apr 2026 00:01:18 GMT
ENV PATH=/usr/local/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Apr 2026 00:01:18 GMT
ENV LANG=C.UTF-8
# Tue, 14 Apr 2026 00:01:18 GMT
ENV JAVA_VERSION=27-ea+17
# Tue, 14 Apr 2026 00:01:18 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/17/GPL/openjdk-27-ea+17_linux-x64_bin.tar.gz'; 			downloadSha256='9052972f914c38a9c00c5d8104a0b58217438f9a672ae7abead7c12347bb0d7c'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/17/GPL/openjdk-27-ea+17_linux-aarch64_bin.tar.gz'; 			downloadSha256='c2be8295243785a5077e17817615b5f355a643367e44eef5972e58fcbd8bde4b'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 14 Apr 2026 00:01:18 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:5435b2dcdf5cb7faa0d5b1d4d54be2c72a776fab9a605336f5067d6e9ecb5976`  
		Last Modified: Tue, 07 Apr 2026 00:11:35 GMT  
		Size: 29.8 MB (29775640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0d7a192164225043592c98b7e5ae919e51ad3376dbdabc2ff7c4699f9bd492b`  
		Last Modified: Tue, 14 Apr 2026 00:01:43 GMT  
		Size: 5.3 MB (5333899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48d503dbd850e5288fd33f1327d13f9f6d8622f27ad27bc86eab53c956df0032`  
		Last Modified: Tue, 14 Apr 2026 00:01:48 GMT  
		Size: 229.0 MB (229020044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-slim-trixie` - unknown; unknown

```console
$ docker pull openjdk@sha256:194a3e41aa28f256473074d99155a9748ccac3ac8f6a3bcf5febff22bfb82408
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2297004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:353a134b682d0e9b85bad4193579f9eae208a0b2f3dbf79b5d2befe33dc43c8f`

```dockerfile
```

-	Layers:
	-	`sha256:3e4e4655d854bb38b753ef70489440b80e7eac2c61c86cfe53e30a641ce0a2dd`  
		Last Modified: Tue, 14 Apr 2026 00:01:42 GMT  
		Size: 2.3 MB (2278895 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:355475453e5a99d6ac847583166156cf99acac1c0e1ea181389c83fa8244b9c7`  
		Last Modified: Tue, 14 Apr 2026 00:01:42 GMT  
		Size: 18.1 KB (18109 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:27-ea-slim-trixie` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:cbb7be97d267b940b750e7b0287c48c9c0bfb3cd374b2d413c0b2a9826549fd0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **262.8 MB (262757375 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e7528318137845a88890d7fd985972cfcfee1643c24b6e5336f93a3dd93fc10`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1775433600'
# Tue, 14 Apr 2026 00:02:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 14 Apr 2026 00:02:33 GMT
ENV JAVA_HOME=/usr/local/openjdk-27
# Tue, 14 Apr 2026 00:02:33 GMT
ENV PATH=/usr/local/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Apr 2026 00:02:33 GMT
ENV LANG=C.UTF-8
# Tue, 14 Apr 2026 00:02:33 GMT
ENV JAVA_VERSION=27-ea+17
# Tue, 14 Apr 2026 00:02:33 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/17/GPL/openjdk-27-ea+17_linux-x64_bin.tar.gz'; 			downloadSha256='9052972f914c38a9c00c5d8104a0b58217438f9a672ae7abead7c12347bb0d7c'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/17/GPL/openjdk-27-ea+17_linux-aarch64_bin.tar.gz'; 			downloadSha256='c2be8295243785a5077e17817615b5f355a643367e44eef5972e58fcbd8bde4b'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 14 Apr 2026 00:02:33 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:53196b1f47bdd6997874156c61491c9a36e115d9b7bd5d74e0cb5c2fc4ee69ce`  
		Last Modified: Tue, 07 Apr 2026 00:11:28 GMT  
		Size: 30.1 MB (30138551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7662c4924e9041a9dd8a31b9a37ef17f0dd822c4dcd69fc98eb4221db63f9d7`  
		Last Modified: Tue, 14 Apr 2026 00:02:53 GMT  
		Size: 5.6 MB (5639504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a7f12bb026852eaafe98f9d8093adf19234b977c0e2d58c2b5035e1449bf0d6`  
		Last Modified: Tue, 14 Apr 2026 00:02:59 GMT  
		Size: 227.0 MB (226979320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-slim-trixie` - unknown; unknown

```console
$ docker pull openjdk@sha256:a4e88068e535837b4b5364f10d10e91214d3b3b0d43afb3ecd490ec5e94bdfb4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2296857 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c872715a025eae20e092981f476b65b18ce5db72cac308e04921210520a92aa`

```dockerfile
```

-	Layers:
	-	`sha256:31a29484ca0c38b12780835daa92a58b7b00e37e915420c9899a142eaa59c4ff`  
		Last Modified: Tue, 14 Apr 2026 00:02:54 GMT  
		Size: 2.3 MB (2278581 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e84128dedc3877549e3ea11aa6304d953aff35aeea2134fd9cd17a59c80dbc3d`  
		Last Modified: Tue, 14 Apr 2026 00:02:53 GMT  
		Size: 18.3 KB (18276 bytes)  
		MIME: application/vnd.in-toto+json
