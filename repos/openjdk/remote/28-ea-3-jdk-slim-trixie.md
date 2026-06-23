## `openjdk:28-ea-3-jdk-slim-trixie`

```console
$ docker pull openjdk@sha256:345b065eae50c6d804de9638100334827f9a340804f567e1fc997b2980938164
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:28-ea-3-jdk-slim-trixie` - linux; amd64

```console
$ docker pull openjdk@sha256:3c52592c915e1be5b3e1382543e42db819666048e0c4657adb7626267db28909
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **259.7 MB (259706336 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f820b682c56be093f625370d108d3422f994df069793fea0441e0709143ff0e2`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1781049600'
# Mon, 22 Jun 2026 22:38:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 22 Jun 2026 22:39:02 GMT
ENV JAVA_HOME=/usr/local/openjdk-28
# Mon, 22 Jun 2026 22:39:02 GMT
ENV PATH=/usr/local/openjdk-28/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jun 2026 22:39:02 GMT
ENV LANG=C.UTF-8
# Mon, 22 Jun 2026 22:39:02 GMT
ENV JAVA_VERSION=28-ea+3
# Mon, 22 Jun 2026 22:39:02 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk28/3/GPL/openjdk-28-ea+3_linux-x64_bin.tar.gz'; 			downloadSha256='44b5bc19b0533fb00a363915f15ee1c9a9514dca2fb5bd56d13c204676ceef67'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk28/3/GPL/openjdk-28-ea+3_linux-aarch64_bin.tar.gz'; 			downloadSha256='12d4698e60552120853334a624fd1d10ffca8386b1c52b0089fc9c607a9d46e8'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Mon, 22 Jun 2026 22:39:02 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:72c03230f1363a3fb61d2f98504cf168bad3fe22f511ad2005dc021515d7ce97`  
		Last Modified: Wed, 10 Jun 2026 23:40:25 GMT  
		Size: 29.8 MB (29785415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e4652e25f8615e2c4a23ccf5a46c7f1463fc3ea010f62725fd59205e21e3dac`  
		Last Modified: Mon, 22 Jun 2026 22:39:22 GMT  
		Size: 2.4 MB (2371321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0f3202e39f93acec3b7bb8c05d0e2b350c62d70fc4dc4f26f9b9052c85bbd52`  
		Last Modified: Mon, 22 Jun 2026 22:39:27 GMT  
		Size: 227.5 MB (227549600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:28-ea-3-jdk-slim-trixie` - unknown; unknown

```console
$ docker pull openjdk@sha256:7a99f5ab7286c6bd6be420ca9f6635139fffe71aaada765e8d1885158e749480
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2294460 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34b3d0cacca055943fa5848e478a96ccfb0077f575f79bb5ac468c8e2beb3511`

```dockerfile
```

-	Layers:
	-	`sha256:66d616beecba91d43f834544ad6e61bfb19fa61c6045379cb2f3958de6a320b7`  
		Last Modified: Mon, 22 Jun 2026 22:39:22 GMT  
		Size: 2.3 MB (2276372 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:53fe4750cfa5fb0455857fb51ff02c19c687e59a9cc0f1d78821077cbcfb9ebe`  
		Last Modified: Mon, 22 Jun 2026 22:39:22 GMT  
		Size: 18.1 KB (18088 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:28-ea-3-jdk-slim-trixie` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:061a0119fd984b218f5ba743b9e91093c07d52063e31548e19441ff0629187e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.1 MB (258052908 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ceba1ff1299fa8bdcd91b5e9b29983b53f42f8f48a0275d000c9130cd455eaa0`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1781049600'
# Mon, 22 Jun 2026 22:38:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 22 Jun 2026 22:38:15 GMT
ENV JAVA_HOME=/usr/local/openjdk-28
# Mon, 22 Jun 2026 22:38:15 GMT
ENV PATH=/usr/local/openjdk-28/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jun 2026 22:38:15 GMT
ENV LANG=C.UTF-8
# Mon, 22 Jun 2026 22:38:15 GMT
ENV JAVA_VERSION=28-ea+3
# Mon, 22 Jun 2026 22:38:15 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk28/3/GPL/openjdk-28-ea+3_linux-x64_bin.tar.gz'; 			downloadSha256='44b5bc19b0533fb00a363915f15ee1c9a9514dca2fb5bd56d13c204676ceef67'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk28/3/GPL/openjdk-28-ea+3_linux-aarch64_bin.tar.gz'; 			downloadSha256='12d4698e60552120853334a624fd1d10ffca8386b1c52b0089fc9c607a9d46e8'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Mon, 22 Jun 2026 22:38:15 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:a25cd16f2d8653f652f8292b34b21bfbabdc85d6b39861a24b85f0896df1a95e`  
		Last Modified: Wed, 10 Jun 2026 23:40:16 GMT  
		Size: 30.1 MB (30148530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7619e8eefd083842b4dfa11f156b925b553c49d13c9e81fa5ae3e36491ec113`  
		Last Modified: Mon, 22 Jun 2026 22:38:36 GMT  
		Size: 2.3 MB (2314517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2f9c6655d9a7a144303bb51a1c7e9a1e73ec938ac213d2b92a70e7c2a783432`  
		Last Modified: Mon, 22 Jun 2026 22:38:42 GMT  
		Size: 225.6 MB (225589861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:28-ea-3-jdk-slim-trixie` - unknown; unknown

```console
$ docker pull openjdk@sha256:4368e44faaec5fded941edd2a28324cdd3203e95a4d5a96bc7813d2c70737305
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2294305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f0645b5fc133108552332d4006ae705f0124e97caa049421a67efc9e71bd1d0`

```dockerfile
```

-	Layers:
	-	`sha256:77687850d1e6d4beeec85587e2d953fd5993c5e469c87520fa0612e1d2cb6d51`  
		Last Modified: Mon, 22 Jun 2026 22:38:36 GMT  
		Size: 2.3 MB (2276050 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:973fc9da8ec2ca5b70c6f9386e47c4ded407c9113b1deeec5b569ce7e1376ce7`  
		Last Modified: Mon, 22 Jun 2026 22:38:35 GMT  
		Size: 18.3 KB (18255 bytes)  
		MIME: application/vnd.in-toto+json
