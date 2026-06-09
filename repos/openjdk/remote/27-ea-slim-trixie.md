## `openjdk:27-ea-slim-trixie`

```console
$ docker pull openjdk@sha256:9829f1f9101d6c3c4afe13a42117dd305d08df0cf1105ef6a5a0696d9800004c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:27-ea-slim-trixie` - linux; amd64

```console
$ docker pull openjdk@sha256:d177851a0add4050d6b9a5b559e3d9719cd569139572e334d3cc3b056cbfb688
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **259.3 MB (259267468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d236e5a9f34c1c0a7d4885d354cf7cc09d16549c58f9c152a032fcaeb786fecd`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1779062400'
# Tue, 09 Jun 2026 20:06:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jun 2026 20:06:16 GMT
ENV JAVA_HOME=/usr/local/openjdk-27
# Tue, 09 Jun 2026 20:06:16 GMT
ENV PATH=/usr/local/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Jun 2026 20:06:16 GMT
ENV LANG=C.UTF-8
# Tue, 09 Jun 2026 20:06:16 GMT
ENV JAVA_VERSION=27-ea+25
# Tue, 09 Jun 2026 20:06:16 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/25/GPL/openjdk-27-ea+25_linux-x64_bin.tar.gz'; 			downloadSha256='6287dc1b8b810fc6fb0ecf2ff0f15464e7bbd5b44c45008588224072bbfbaa87'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/25/GPL/openjdk-27-ea+25_linux-aarch64_bin.tar.gz'; 			downloadSha256='6f13903699316f8ee6089a0551ef28686b3bae5b195a98cc4051b365819396cb'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 09 Jun 2026 20:06:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:5b4d6ff92fc4e14e911b7753c954fac965d48c40fe1075758d284148ccace970`  
		Last Modified: Tue, 19 May 2026 22:37:05 GMT  
		Size: 29.8 MB (29779926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:244436431afbda7ba4bd03320975fa10d6b2ddbe7198014824ff0f625fd845e9`  
		Last Modified: Tue, 09 Jun 2026 20:06:36 GMT  
		Size: 2.4 MB (2371344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42fd0a4442acdb0aa3c188ee8b542e967e94356ecd2a1fe703668f22adc85b19`  
		Last Modified: Tue, 09 Jun 2026 20:06:40 GMT  
		Size: 227.1 MB (227116198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-slim-trixie` - unknown; unknown

```console
$ docker pull openjdk@sha256:33928ed667bd1c60fe975f6c49331afc635520da0d21162e9c0173f99c6f556f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2294493 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88c761e81125b52c2cf71a9e13184cebe80969dbe4f1581191c27c5be223415a`

```dockerfile
```

-	Layers:
	-	`sha256:07e67bbcd8ff508003ed7bff19ae17fa46c943395bb42a7db0bdec52c5a8a9a7`  
		Last Modified: Tue, 09 Jun 2026 20:06:36 GMT  
		Size: 2.3 MB (2276384 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:da653d534b61c0f6225b58aacea0d0fd48d37ca36e50ecf9df6131bb082471cd`  
		Last Modified: Tue, 09 Jun 2026 20:06:36 GMT  
		Size: 18.1 KB (18109 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:27-ea-slim-trixie` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:231307934b5827459fb68a85eb30a4bb1939632417888b47946fa8b00a421db4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.6 MB (257555451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56ed7a18c66b0700d9ae0d1e3888b5d205da332c3923e0c21b00fde472171cfd`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1779062400'
# Tue, 09 Jun 2026 20:05:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jun 2026 20:05:44 GMT
ENV JAVA_HOME=/usr/local/openjdk-27
# Tue, 09 Jun 2026 20:05:44 GMT
ENV PATH=/usr/local/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Jun 2026 20:05:44 GMT
ENV LANG=C.UTF-8
# Tue, 09 Jun 2026 20:05:44 GMT
ENV JAVA_VERSION=27-ea+25
# Tue, 09 Jun 2026 20:05:44 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/25/GPL/openjdk-27-ea+25_linux-x64_bin.tar.gz'; 			downloadSha256='6287dc1b8b810fc6fb0ecf2ff0f15464e7bbd5b44c45008588224072bbfbaa87'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/25/GPL/openjdk-27-ea+25_linux-aarch64_bin.tar.gz'; 			downloadSha256='6f13903699316f8ee6089a0551ef28686b3bae5b195a98cc4051b365819396cb'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 09 Jun 2026 20:05:44 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:cda3d70ae7d7c3d0b3b57a99a2085f9d93e919a846913dc6517a420b348c123d`  
		Last Modified: Tue, 19 May 2026 22:36:58 GMT  
		Size: 30.1 MB (30141919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a14b387935bd74dee1a7965c79c7cbdf87d29ead065a55027458da9865777b67`  
		Last Modified: Tue, 09 Jun 2026 20:06:04 GMT  
		Size: 2.3 MB (2314539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b26cf7fe984bd81ff79604cdf3b56c5c4b47c69db59af31d1d5710a58e3d8bbd`  
		Last Modified: Tue, 09 Jun 2026 20:06:12 GMT  
		Size: 225.1 MB (225098993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-slim-trixie` - unknown; unknown

```console
$ docker pull openjdk@sha256:223fb6b5d22981892b3f206784b23f9e5dcf1f644a93d937dfe3204ee386b675
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2294338 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4871c52d0f8f53ce0fa65582add7e89d7698f7a39f38a0e06739be91acb8496`

```dockerfile
```

-	Layers:
	-	`sha256:8c0862558e1ba3e15ab8bb2b1cc7f32024eca1e50b706fa02dc3fa8c67fdf28e`  
		Last Modified: Tue, 09 Jun 2026 20:06:04 GMT  
		Size: 2.3 MB (2276062 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1e2ce2410332fc036ee11ce2ca2a2d98bdb649b7ca8574db0af227e7915b90cb`  
		Last Modified: Tue, 09 Jun 2026 20:06:04 GMT  
		Size: 18.3 KB (18276 bytes)  
		MIME: application/vnd.in-toto+json
