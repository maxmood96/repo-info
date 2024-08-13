## `openjdk:23-jdk-slim-bookworm`

```console
$ docker pull openjdk@sha256:d2f76b376d2e37072fed67a8303a5e5f49a06423712ca40f508b6560ff119ed4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:23-jdk-slim-bookworm` - linux; amd64

```console
$ docker pull openjdk@sha256:777854948772a66ed05d4bee662ad70010d99494c21543fbce0964566921b8b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.6 MB (244618428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b94a46cfee11ca30ca917b1f49709eeccbd2543c996f9104a5bfe0f2c1999de1`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 09 Aug 2024 18:48:11 GMT
ADD file:3d9897cfe027ecc7cbdb16e74a676ed143725ea2d08dbb0dde23309e041de0f3 in / 
# Fri, 09 Aug 2024 18:48:11 GMT
CMD ["bash"]
# Fri, 09 Aug 2024 18:48:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 09 Aug 2024 18:48:11 GMT
ENV JAVA_HOME=/usr/local/openjdk-23
# Fri, 09 Aug 2024 18:48:11 GMT
ENV PATH=/usr/local/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 09 Aug 2024 18:48:11 GMT
ENV LANG=C.UTF-8
# Fri, 09 Aug 2024 18:48:11 GMT
ENV JAVA_VERSION=23
# Fri, 09 Aug 2024 18:48:11 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/GA/jdk23/3c5b90190c68498b986a97f276efd28a/36/GPL/openjdk-23_linux-x64_bin.tar.gz'; 			downloadSha256='d8d169ae7a0285e09872565bc3044ad97697d3780e678d2a5ae9f8451c207cfc'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/GA/jdk23/3c5b90190c68498b986a97f276efd28a/36/GPL/openjdk-23_linux-aarch64_bin.tar.gz'; 			downloadSha256='5cad336e22d64a4a578f59d089223c226d67455c410cbaeb91f5fa0503ce2f96'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 09 Aug 2024 18:48:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:e4fff0779e6ddd22366469f08626c3ab1884b5cbe1719b26da238c95f247b305`  
		Last Modified: Tue, 13 Aug 2024 00:23:48 GMT  
		Size: 29.1 MB (29126232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07e96879dafd5fcad150f47de5cdce2190ed735517f3710482dd5157d5bbb29f`  
		Last Modified: Tue, 13 Aug 2024 01:12:28 GMT  
		Size: 4.0 MB (4016742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:556322af541dba090796fecdafb6dbd4644a3c4cbe73c06355040ef054a0caf0`  
		Last Modified: Tue, 13 Aug 2024 01:12:31 GMT  
		Size: 211.5 MB (211475454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-jdk-slim-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:67dd939bc2a918ac90b240bb816d5694c27ed944f07c56e3392bf4d8588de935
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2381976 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:147cfc6c527f20da8865f99a332497a37c49805ac1726318a84b0ad63d2facf8`

```dockerfile
```

-	Layers:
	-	`sha256:9140fcde82153919d7685ff1c16eb3b84ad170927f9b29a6dedf4820ac05d9bf`  
		Last Modified: Tue, 13 Aug 2024 01:12:28 GMT  
		Size: 2.4 MB (2363986 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b8d2c341d406da2d006a13c8b6d23dc95c48b9aac96760b155a35729fa8068c2`  
		Last Modified: Tue, 13 Aug 2024 01:12:27 GMT  
		Size: 18.0 KB (17990 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:23-jdk-slim-bookworm` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:bd1ca83adeb75925a6384394ace0683d36c79f2c8d3f44cc62fa18ce4f951480
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.3 MB (242327013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb6aff07b8e84c5ecfc90cc4b3d17a98c8ab5728265ce3960d5b3d6347bff030`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 23 Jul 2024 04:17:51 GMT
ADD file:9b9556e1f3168a82eb85577dc07d85b2e7c1a72c5c35a4003f00042dd27b4fa2 in / 
# Tue, 23 Jul 2024 04:17:52 GMT
CMD ["bash"]
# Fri, 09 Aug 2024 18:48:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 09 Aug 2024 18:48:11 GMT
ENV JAVA_HOME=/usr/local/openjdk-23
# Fri, 09 Aug 2024 18:48:11 GMT
ENV PATH=/usr/local/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 09 Aug 2024 18:48:11 GMT
ENV LANG=C.UTF-8
# Fri, 09 Aug 2024 18:48:11 GMT
ENV JAVA_VERSION=23
# Fri, 09 Aug 2024 18:48:11 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/GA/jdk23/3c5b90190c68498b986a97f276efd28a/36/GPL/openjdk-23_linux-x64_bin.tar.gz'; 			downloadSha256='d8d169ae7a0285e09872565bc3044ad97697d3780e678d2a5ae9f8451c207cfc'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/GA/jdk23/3c5b90190c68498b986a97f276efd28a/36/GPL/openjdk-23_linux-aarch64_bin.tar.gz'; 			downloadSha256='5cad336e22d64a4a578f59d089223c226d67455c410cbaeb91f5fa0503ce2f96'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 09 Aug 2024 18:48:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:262a5f25eec7a7daccd94a64695e41acca5262f481c3630ef31289616897aa40`  
		Last Modified: Tue, 23 Jul 2024 04:20:29 GMT  
		Size: 29.2 MB (29156571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c349375e2e294f7eff4dd86f726854408dbf40098a96b9250ed96a5be15a73f5`  
		Last Modified: Mon, 29 Jul 2024 16:59:58 GMT  
		Size: 3.8 MB (3829955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:929fa83a74843eecac518f68733b830deeb3278c05c41ea6271180f749bf2071`  
		Last Modified: Mon, 12 Aug 2024 18:37:52 GMT  
		Size: 209.3 MB (209340487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-jdk-slim-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:3a804be84ef0135fa14d9b611f401211d8639780045a074585922a9a98a872ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2382639 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75806259a2d5a423161c767ba0207439e68440b641a43dbe31f5fbc7fef3022c`

```dockerfile
```

-	Layers:
	-	`sha256:639cd2612d39972f3f3aeb3de754945c953b47ebac5f1f36ba7aab17270ff1d1`  
		Last Modified: Mon, 12 Aug 2024 18:37:47 GMT  
		Size: 2.4 MB (2364292 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:888f4bc311027cd4b669cd2b9b109b4685ec75c788d0dab38bffb1006e25e70a`  
		Last Modified: Mon, 12 Aug 2024 18:37:47 GMT  
		Size: 18.3 KB (18347 bytes)  
		MIME: application/vnd.in-toto+json
