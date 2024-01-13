## `openjdk:23-ea-5-slim`

```console
$ docker pull openjdk@sha256:7249d61899b0c8d4d28400800c8b6370f10418d79f3efb0077c05d361ebae893
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:23-ea-5-slim` - linux; amd64

```console
$ docker pull openjdk@sha256:ee7f8810f3e7ece2af71cfde5f2d213bb94c5d47a05f2c89eb67febd2e2883bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.4 MB (236367046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62b74173e3f1b6fc74442ce69c5b3e1f4c3cec8cc8d914f67d91b4c870b77f6e`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 11 Jan 2024 02:37:54 GMT
ADD file:9deb26e1dbc258df47629e6f8fbcea4e4b54e7673537cc925db16af858d9cc8d in / 
# Thu, 11 Jan 2024 02:37:54 GMT
CMD ["bash"]
# Fri, 12 Jan 2024 02:00:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 12 Jan 2024 02:00:35 GMT
ENV JAVA_HOME=/usr/local/openjdk-23
# Fri, 12 Jan 2024 02:00:35 GMT
ENV PATH=/usr/local/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Jan 2024 02:00:35 GMT
ENV LANG=C.UTF-8
# Fri, 12 Jan 2024 02:00:35 GMT
ENV JAVA_VERSION=23-ea+5
# Fri, 12 Jan 2024 02:00:35 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/5/GPL/openjdk-23-ea+5_linux-x64_bin.tar.gz'; 			downloadSha256='ccf927cccbf0ae655b04e2da009aa13811e971f214fee242acd46ca2b5d9ed63'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/5/GPL/openjdk-23-ea+5_linux-aarch64_bin.tar.gz'; 			downloadSha256='acfc5986d442c5c3c3d622e774e0bc9cce3763f485a9a3b71a46a93a3f703d81'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 12 Jan 2024 02:00:35 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2f44b7a888fa005d07c031d3cfad2a1c0344207def2ab9dbb97712425ff812c1`  
		Last Modified: Thu, 11 Jan 2024 02:42:28 GMT  
		Size: 29.1 MB (29125921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a798c28dcb1119dc29bb4785cc742f0718b14571656cc2a62709a497104b5da`  
		Last Modified: Sat, 13 Jan 2024 01:07:30 GMT  
		Size: 4.0 MB (4014834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:488edf08e3f067f75c163607479d07ebcd60ee3b2015f8e7c3c27cda01c802fb`  
		Last Modified: Sat, 13 Jan 2024 01:07:36 GMT  
		Size: 203.2 MB (203226291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-ea-5-slim` - unknown; unknown

```console
$ docker pull openjdk@sha256:b1c0c5f6c48506518b9423f14783bda3bdf3f2df311aa4bc89ef034c90313e23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2056501 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3a0067c7afeb2f8b35586212fb98a350a79552d6d78bdcf58fd88b920c80703`

```dockerfile
```

-	Layers:
	-	`sha256:61da708d7db1e3ff6a0f02c837747841ed7d43275f23dc7c1830e28df9af6aff`  
		Last Modified: Sat, 13 Jan 2024 01:07:30 GMT  
		Size: 2.0 MB (2037175 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d50c89ba4ceb6ef1dbcef1e17fd48fdd43ccdda234d1bbbe90d1e50301c9aad5`  
		Last Modified: Sat, 13 Jan 2024 01:07:29 GMT  
		Size: 19.3 KB (19326 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:23-ea-5-slim` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:c7d0379e5f291fabb9ab194d19a5a29d6d2e34707d9982c60c00d4456832555b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.1 MB (234120302 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:471521b16824860003648cb82c4455f8cc367ab551f0ae8eab9596806efeeded`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 11 Jan 2024 02:40:44 GMT
ADD file:70e4f0c71f88c97c8db279b998c10d4943954d304ff9f51875c3699a4dc5ee4e in / 
# Thu, 11 Jan 2024 02:40:45 GMT
CMD ["bash"]
# Fri, 12 Jan 2024 02:00:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 12 Jan 2024 02:00:35 GMT
ENV JAVA_HOME=/usr/local/openjdk-23
# Fri, 12 Jan 2024 02:00:35 GMT
ENV PATH=/usr/local/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Jan 2024 02:00:35 GMT
ENV LANG=C.UTF-8
# Fri, 12 Jan 2024 02:00:35 GMT
ENV JAVA_VERSION=23-ea+5
# Fri, 12 Jan 2024 02:00:35 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/5/GPL/openjdk-23-ea+5_linux-x64_bin.tar.gz'; 			downloadSha256='ccf927cccbf0ae655b04e2da009aa13811e971f214fee242acd46ca2b5d9ed63'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/5/GPL/openjdk-23-ea+5_linux-aarch64_bin.tar.gz'; 			downloadSha256='acfc5986d442c5c3c3d622e774e0bc9cce3763f485a9a3b71a46a93a3f703d81'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 12 Jan 2024 02:00:35 GMT
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
	-	`sha256:0956527ad8f1e6f5a5b90e8e95980b3c5631b88b66e18549f03dcaee44a81844`  
		Last Modified: Sat, 13 Jan 2024 01:40:35 GMT  
		Size: 201.1 MB (201143069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-ea-5-slim` - unknown; unknown

```console
$ docker pull openjdk@sha256:d0337503d39d1d87b2ec348b46863e01f1ab1b6ca7d89bc213df1eb5ea281037
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2055739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c133276fdd224b285cf6be39057d2eef3414bf41d352eb6c51990dd1d561c7a0`

```dockerfile
```

-	Layers:
	-	`sha256:67b21929b1e463c3baa620907a29297d9d54a4d124fba1f5be3313b052115006`  
		Last Modified: Sat, 13 Jan 2024 01:40:30 GMT  
		Size: 2.0 MB (2036553 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1a31b6f1fe3746e5cbc4f48c58cc5b4a21b145fad605dadea5dd982b22d962ac`  
		Last Modified: Sat, 13 Jan 2024 01:40:29 GMT  
		Size: 19.2 KB (19186 bytes)  
		MIME: application/vnd.in-toto+json
