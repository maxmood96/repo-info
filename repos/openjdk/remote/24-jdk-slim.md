## `openjdk:24-jdk-slim`

```console
$ docker pull openjdk@sha256:e056ba98b15309929d24bcffe06d0446370ebb0ec7b56be260316ad2e32e4d5c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:24-jdk-slim` - linux; amd64

```console
$ docker pull openjdk@sha256:49388648a4524f1d8837213fc569cceb5a7ae0e21fd7a0c31c431fb7837508e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **245.1 MB (245062525 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4480b773d51fb4afb2416919d412ed8b06e83f0e00f480b4d510e4a85f5993ab`
-	Default Command: `["jshell"]`

```dockerfile
# Sat, 10 Aug 2024 00:48:15 GMT
ADD file:3d9897cfe027ecc7cbdb16e74a676ed143725ea2d08dbb0dde23309e041de0f3 in / 
# Sat, 10 Aug 2024 00:48:15 GMT
CMD ["bash"]
# Sat, 10 Aug 2024 00:48:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 10 Aug 2024 00:48:15 GMT
ENV JAVA_HOME=/usr/local/openjdk-24
# Sat, 10 Aug 2024 00:48:15 GMT
ENV PATH=/usr/local/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 10 Aug 2024 00:48:15 GMT
ENV LANG=C.UTF-8
# Sat, 10 Aug 2024 00:48:15 GMT
ENV JAVA_VERSION=24-ea+10
# Sat, 10 Aug 2024 00:48:15 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/10/GPL/openjdk-24-ea+10_linux-x64_bin.tar.gz'; 			downloadSha256='b4c878f685a1333de0743bc33fb94a6cbd60e1ddda7e1d88068c2acc1c91012b'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/10/GPL/openjdk-24-ea+10_linux-aarch64_bin.tar.gz'; 			downloadSha256='3640a7ecb431e631d5d23e96d0df679fb45cfed38f527a3810caeebebc44a3a5'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 10 Aug 2024 00:48:15 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:e4fff0779e6ddd22366469f08626c3ab1884b5cbe1719b26da238c95f247b305`  
		Last Modified: Tue, 13 Aug 2024 00:23:48 GMT  
		Size: 29.1 MB (29126232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3815d767a89dca203f726893d25c523ada1f2e382858189bf07fff7fb07af00`  
		Last Modified: Tue, 13 Aug 2024 01:12:23 GMT  
		Size: 4.0 MB (4016754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c2a69a4356a1421a7bc9f696c6866ca4b918b102eab307619e21dab07ede173`  
		Last Modified: Tue, 13 Aug 2024 01:12:25 GMT  
		Size: 211.9 MB (211919539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-jdk-slim` - unknown; unknown

```console
$ docker pull openjdk@sha256:7c33521eb646fc38d7351e4fb9b206eed14100fc18c00451c7aeabfbfeeafcb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2384536 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9610db2cb305ea8c407fdf4faa0458632e9cb1ca235d5a2a44334e9454c2a267`

```dockerfile
```

-	Layers:
	-	`sha256:328bd08330ce97f00a0190e1067936034e7cf55699596102e10e6130528e1a8d`  
		Last Modified: Tue, 13 Aug 2024 01:12:23 GMT  
		Size: 2.4 MB (2365306 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:decfacd19e85f9b81eb1aec72a840e44ac89e49843fa7e116cb8c128861467c1`  
		Last Modified: Tue, 13 Aug 2024 01:12:22 GMT  
		Size: 19.2 KB (19230 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:24-jdk-slim` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:21bdbc02c2280ff535f3d44ca167ec41a0c68b63548fd42be27bf77a1dba372d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.8 MB (242754088 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e726aadff6dce0c56d175d0d6759f6502d047e57f6d26f9e8f700b1b28449bd`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 23 Jul 2024 04:17:51 GMT
ADD file:9b9556e1f3168a82eb85577dc07d85b2e7c1a72c5c35a4003f00042dd27b4fa2 in / 
# Tue, 23 Jul 2024 04:17:52 GMT
CMD ["bash"]
# Sat, 10 Aug 2024 00:48:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 10 Aug 2024 00:48:15 GMT
ENV JAVA_HOME=/usr/local/openjdk-24
# Sat, 10 Aug 2024 00:48:15 GMT
ENV PATH=/usr/local/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 10 Aug 2024 00:48:15 GMT
ENV LANG=C.UTF-8
# Sat, 10 Aug 2024 00:48:15 GMT
ENV JAVA_VERSION=24-ea+10
# Sat, 10 Aug 2024 00:48:15 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/10/GPL/openjdk-24-ea+10_linux-x64_bin.tar.gz'; 			downloadSha256='b4c878f685a1333de0743bc33fb94a6cbd60e1ddda7e1d88068c2acc1c91012b'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/10/GPL/openjdk-24-ea+10_linux-aarch64_bin.tar.gz'; 			downloadSha256='3640a7ecb431e631d5d23e96d0df679fb45cfed38f527a3810caeebebc44a3a5'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 10 Aug 2024 00:48:15 GMT
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
	-	`sha256:1a27b1e8c454d5fc9ef44c174e7c59731571a03a7a5be6efa983d1e6a23f949f`  
		Last Modified: Mon, 12 Aug 2024 18:32:21 GMT  
		Size: 209.8 MB (209767562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-jdk-slim` - unknown; unknown

```console
$ docker pull openjdk@sha256:4796e08eb4c88a5959097099625e4cb89583cc157929dbea4f045e21a47340b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2385294 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd8e4cb5343d0086fe7fc5df3fb0d60dd9c864503ca5a8c77c97ef88d2def75f`

```dockerfile
```

-	Layers:
	-	`sha256:997d2b260140a9e4e604add0b22806b25f2d03b27180a07323c9fcf0ca888fdf`  
		Last Modified: Mon, 12 Aug 2024 18:32:16 GMT  
		Size: 2.4 MB (2365660 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:963109d73b5583f3633c22534c6228ca84fb2d33086116b73f7f93b23ef1f461`  
		Last Modified: Mon, 12 Aug 2024 18:32:16 GMT  
		Size: 19.6 KB (19634 bytes)  
		MIME: application/vnd.in-toto+json
