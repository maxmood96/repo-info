## `openjdk:22-ea-jdk-slim`

```console
$ docker pull openjdk@sha256:c38fe4dbd6f53acca99d20ac4842adb4662f7b251dc5207e84e678ab19e86013
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:22-ea-jdk-slim` - linux; amd64

```console
$ docker pull openjdk@sha256:df66faae2ba97e9f0165a8a8e2d9c815c8112f9bd7e10b16bfa8ef3c1c1fb2bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.1 MB (236066039 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c83e10990b6da9b6860c98cffda32dfd9e5559ff7b9ece22627feed8637df8e`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 11 Jan 2024 02:37:54 GMT
ADD file:9deb26e1dbc258df47629e6f8fbcea4e4b54e7673537cc925db16af858d9cc8d in / 
# Thu, 11 Jan 2024 02:37:54 GMT
CMD ["bash"]
# Fri, 12 Jan 2024 01:48:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 12 Jan 2024 01:48:33 GMT
ENV JAVA_HOME=/usr/local/openjdk-22
# Fri, 12 Jan 2024 01:48:33 GMT
ENV PATH=/usr/local/openjdk-22/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Jan 2024 01:48:33 GMT
ENV LANG=C.UTF-8
# Fri, 12 Jan 2024 01:48:33 GMT
ENV JAVA_VERSION=22-ea+31
# Fri, 12 Jan 2024 01:48:33 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/31/GPL/openjdk-22-ea+31_linux-x64_bin.tar.gz'; 			downloadSha256='389969d79769fb950fcaa9960610f90497af6fffb08bcbf1a88603450b58dc29'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/31/GPL/openjdk-22-ea+31_linux-aarch64_bin.tar.gz'; 			downloadSha256='662b370c327124f56151ec75cb7867c08a621c32eb8fdb2eabb0505af36331ce'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 12 Jan 2024 01:48:33 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2f44b7a888fa005d07c031d3cfad2a1c0344207def2ab9dbb97712425ff812c1`  
		Last Modified: Thu, 11 Jan 2024 02:42:28 GMT  
		Size: 29.1 MB (29125921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:621e4a3ee7915e6e2b1caad6d77ff478d46cc7646055833df3dfb2b18144946e`  
		Last Modified: Sat, 13 Jan 2024 01:07:21 GMT  
		Size: 4.0 MB (4014840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0bbe648769b5d117e6420e22c4bb9201bddcf362aa57eadc9ad73e15a21d919`  
		Last Modified: Sat, 13 Jan 2024 01:07:24 GMT  
		Size: 202.9 MB (202925278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:22-ea-jdk-slim` - unknown; unknown

```console
$ docker pull openjdk@sha256:b91a127e2e972894603ed43f0472280d7bf4a198432ed1ab6cbe107149e11706
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2056531 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98668a2bfba12eb30e7bd3584197f835904305c65a663e7c5f5980c04b0acc99`

```dockerfile
```

-	Layers:
	-	`sha256:56a091f927e94c30d29394f8047be9fb9b64fdb63dc8f703cc89533904540600`  
		Last Modified: Sat, 13 Jan 2024 01:07:20 GMT  
		Size: 2.0 MB (2037187 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ba7bee77437eef76f406157eaf1f3389a8ac837a4d34979832dd4822b82d8f41`  
		Last Modified: Sat, 13 Jan 2024 01:07:20 GMT  
		Size: 19.3 KB (19344 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:22-ea-jdk-slim` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:d37908adada5e3eb3867bac9e79b5ed910e2583a2e46e0d1b0af1457a573eabb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.0 MB (233963580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2491524401e7c8c6bf6cd35e8db7e3ea6d77ffb72677b29ea5477de7cfce0297`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 11 Jan 2024 02:40:44 GMT
ADD file:70e4f0c71f88c97c8db279b998c10d4943954d304ff9f51875c3699a4dc5ee4e in / 
# Thu, 11 Jan 2024 02:40:45 GMT
CMD ["bash"]
# Fri, 12 Jan 2024 01:48:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 12 Jan 2024 01:48:33 GMT
ENV JAVA_HOME=/usr/local/openjdk-22
# Fri, 12 Jan 2024 01:48:33 GMT
ENV PATH=/usr/local/openjdk-22/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Jan 2024 01:48:33 GMT
ENV LANG=C.UTF-8
# Fri, 12 Jan 2024 01:48:33 GMT
ENV JAVA_VERSION=22-ea+31
# Fri, 12 Jan 2024 01:48:33 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/31/GPL/openjdk-22-ea+31_linux-x64_bin.tar.gz'; 			downloadSha256='389969d79769fb950fcaa9960610f90497af6fffb08bcbf1a88603450b58dc29'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/31/GPL/openjdk-22-ea+31_linux-aarch64_bin.tar.gz'; 			downloadSha256='662b370c327124f56151ec75cb7867c08a621c32eb8fdb2eabb0505af36331ce'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 12 Jan 2024 01:48:33 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:a5573528b1f0cf2f5d87c94fe0aee9d8967d5de98258be9303c3c6fa477824ec`  
		Last Modified: Thu, 11 Jan 2024 02:44:04 GMT  
		Size: 29.2 MB (29157335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de02c32dbc1d28978f53ca6d486c22aad0fc165410ea327c587d4a6ac0500e85`  
		Last Modified: Fri, 12 Jan 2024 09:21:39 GMT  
		Size: 3.8 MB (3819898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f47a93bc049bddaad6884414f500bca8f56b8b0ba5dcb167783d220dca5a9337`  
		Last Modified: Sat, 13 Jan 2024 01:45:59 GMT  
		Size: 201.0 MB (200986347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:22-ea-jdk-slim` - unknown; unknown

```console
$ docker pull openjdk@sha256:9f000d270b48550f65897d89de4674841876daf366631d9f997c3f910533260c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2055764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5d24ca766662fd22f054dc1699ab32bcdc9d5297a98eefe1b516d118132295e`

```dockerfile
```

-	Layers:
	-	`sha256:e442f6d19b798db3adbb17fd3184ef0d513b3f5287cce3bf06e0119f6762b1f3`  
		Last Modified: Sat, 13 Jan 2024 01:45:54 GMT  
		Size: 2.0 MB (2036561 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:76d9a91a436295cf843d955d359ebad3124fc0b0c565575aa8f39ab9e8da1d88`  
		Last Modified: Sat, 13 Jan 2024 01:45:54 GMT  
		Size: 19.2 KB (19203 bytes)  
		MIME: application/vnd.in-toto+json
