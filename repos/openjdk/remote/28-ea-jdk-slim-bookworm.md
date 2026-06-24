## `openjdk:28-ea-jdk-slim-bookworm`

```console
$ docker pull openjdk@sha256:7f61623740cd184752ef4ad53e1decd0e2e99498d54326266dacf39aa8e2536a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:28-ea-jdk-slim-bookworm` - linux; amd64

```console
$ docker pull openjdk@sha256:d541b7b60b1fb293001eda00537cc6f91ad69f928632c2dbef9948d863c7b3fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **259.8 MB (259820344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbe5b205b5f6c3aafbd4e65be527d931b114bd0566364e4f244557b905b2c6f8`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1782172800'
# Wed, 24 Jun 2026 01:46:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 01:46:49 GMT
ENV JAVA_HOME=/usr/local/openjdk-28
# Wed, 24 Jun 2026 01:46:49 GMT
ENV PATH=/usr/local/openjdk-28/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 01:46:49 GMT
ENV LANG=C.UTF-8
# Wed, 24 Jun 2026 01:46:49 GMT
ENV JAVA_VERSION=28-ea+3
# Wed, 24 Jun 2026 01:46:49 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk28/3/GPL/openjdk-28-ea+3_linux-x64_bin.tar.gz'; 			downloadSha256='44b5bc19b0533fb00a363915f15ee1c9a9514dca2fb5bd56d13c204676ceef67'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk28/3/GPL/openjdk-28-ea+3_linux-aarch64_bin.tar.gz'; 			downloadSha256='12d4698e60552120853334a624fd1d10ffca8386b1c52b0089fc9c607a9d46e8'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Wed, 24 Jun 2026 01:46:49 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:68629629b516c3cd6f5e71ffbe18e32afb1ae5b4926c92d058c0f11ef1fd58a3`  
		Last Modified: Wed, 24 Jun 2026 00:27:52 GMT  
		Size: 28.2 MB (28237639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abe9db54c86d7a68d27e59fb412c8f13efe8e3ad380636ffc29a3418c6a18f4c`  
		Last Modified: Wed, 24 Jun 2026 01:47:10 GMT  
		Size: 4.0 MB (4032937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7daaf3d1debcd6e50dced5c784c881f4225e6b2e60a96276923d7a46b5a65c2b`  
		Last Modified: Wed, 24 Jun 2026 01:47:15 GMT  
		Size: 227.5 MB (227549768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:28-ea-jdk-slim-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:def1294a6870fe65ab5ec7927b441d3bf0fca5f1dc36de75e90b73eb372d4904
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2664140 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:129c2fd9a73a532ae549c72035cd15ff24f0ca667a9df39ef2bc08aec9c10821`

```dockerfile
```

-	Layers:
	-	`sha256:05aceee363eba7ad1c6d409c1a94f1772dbc2323172466eaab4b19538899ebbe`  
		Last Modified: Wed, 24 Jun 2026 01:47:10 GMT  
		Size: 2.6 MB (2647282 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5ad2fb54a31f68e424bf383a2e778c3d8ee49fa291c6b930ca3dd65f010ad9a8`  
		Last Modified: Wed, 24 Jun 2026 01:47:09 GMT  
		Size: 16.9 KB (16858 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:28-ea-jdk-slim-bookworm` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:2349aec85675f38257af1e8dab5eb88d6461736a8c1c497b16db308033fe2ab5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.6 MB (257563927 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a5bfdb545e2b5d09253a2214c71088021ee114d355abb0f3e614f51ea8f8d45`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1782172800'
# Wed, 24 Jun 2026 01:50:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 01:50:18 GMT
ENV JAVA_HOME=/usr/local/openjdk-28
# Wed, 24 Jun 2026 01:50:18 GMT
ENV PATH=/usr/local/openjdk-28/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 01:50:18 GMT
ENV LANG=C.UTF-8
# Wed, 24 Jun 2026 01:50:18 GMT
ENV JAVA_VERSION=28-ea+3
# Wed, 24 Jun 2026 01:50:18 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk28/3/GPL/openjdk-28-ea+3_linux-x64_bin.tar.gz'; 			downloadSha256='44b5bc19b0533fb00a363915f15ee1c9a9514dca2fb5bd56d13c204676ceef67'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk28/3/GPL/openjdk-28-ea+3_linux-aarch64_bin.tar.gz'; 			downloadSha256='12d4698e60552120853334a624fd1d10ffca8386b1c52b0089fc9c607a9d46e8'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Wed, 24 Jun 2026 01:50:18 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:74f1dcfcc9c80045f6f6394ffcfc261cb19d0c71b97e964aec3d4abf4e0f7009`  
		Last Modified: Wed, 24 Jun 2026 00:27:48 GMT  
		Size: 28.1 MB (28122418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abc9790605ad6479dd03097b56195cd78421f6ef47971d1d6f36e02d93af3769`  
		Last Modified: Wed, 24 Jun 2026 01:50:39 GMT  
		Size: 3.9 MB (3852896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc8bda435e88adf122f67563a65badd964772f0e1cd902fee8a80ef26c3f2f5a`  
		Last Modified: Wed, 24 Jun 2026 01:50:45 GMT  
		Size: 225.6 MB (225588613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:28-ea-jdk-slim-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:1555e4ad485d0becafd6117db61fce4f5faa5d91104839ef9bd4d328a18fcfb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2663893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c317ce064763f208674af578e99bef447ce2fd345e7639e280f60c7ff938630e`

```dockerfile
```

-	Layers:
	-	`sha256:25e6d00d170d414db3e96f6312840f369c7f7b5743a310bbb408d535c3531fa5`  
		Last Modified: Wed, 24 Jun 2026 01:50:39 GMT  
		Size: 2.6 MB (2646916 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e0849f616b41302db616886e4804bb21a909eac18e77f3e3aa5e76ffd2e02cdf`  
		Last Modified: Wed, 24 Jun 2026 01:50:39 GMT  
		Size: 17.0 KB (16977 bytes)  
		MIME: application/vnd.in-toto+json
