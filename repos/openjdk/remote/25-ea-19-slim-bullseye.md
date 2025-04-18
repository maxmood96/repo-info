## `openjdk:25-ea-19-slim-bullseye`

```console
$ docker pull openjdk@sha256:38748740dfa0935705a2e04c95bd8cdd525928a02d40aaeba16d087694732e36
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:25-ea-19-slim-bullseye` - linux; amd64

```console
$ docker pull openjdk@sha256:4a020deb91edde714e81e60ead76ee1fab78a8c42696811606afe174e526864e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.4 MB (244375804 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49a24978600d14cc7d03536255f8abfe30f4c1e6af9027170f2bca007074f01c`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 07 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1743984000'
# Fri, 18 Apr 2025 00:48:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 18 Apr 2025 00:48:12 GMT
ENV JAVA_HOME=/usr/local/openjdk-25
# Fri, 18 Apr 2025 00:48:12 GMT
ENV PATH=/usr/local/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 18 Apr 2025 00:48:12 GMT
ENV LANG=C.UTF-8
# Fri, 18 Apr 2025 00:48:12 GMT
ENV JAVA_VERSION=25-ea+19
# Fri, 18 Apr 2025 00:48:12 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/19/GPL/openjdk-25-ea+19_linux-x64_bin.tar.gz'; 			downloadSha256='5d10a87dcb2a162df9f7ab0c97cc77eff71c53ad442cbf40cce33b8ab6ab117a'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/19/GPL/openjdk-25-ea+19_linux-aarch64_bin.tar.gz'; 			downloadSha256='1324cfa105b4ce10e2ab854c20d7e1a4eda81fb6a1df35dacadc8d65b0b59351'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 18 Apr 2025 00:48:12 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:b983e127c643116d446fa1b64216f464e1d06a8bfaeeb8a895c361c1bc3f5652`  
		Last Modified: Tue, 08 Apr 2025 00:23:09 GMT  
		Size: 30.3 MB (30257419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:523a81127437ef86459e6ec06522d164d839fd2a4d6b8055ddd2d9b1b88206cc`  
		Last Modified: Fri, 18 Apr 2025 18:37:43 GMT  
		Size: 1.6 MB (1581830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c99703b932d8fcfa4ed87e3e909239113dc7fa8a423b2b49b0dad870292df403`  
		Last Modified: Fri, 18 Apr 2025 18:37:46 GMT  
		Size: 212.5 MB (212536555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-ea-19-slim-bullseye` - unknown; unknown

```console
$ docker pull openjdk@sha256:ab0181d9bce21a8fdd3e0c1807b2703dbb1cde5d8f7418c507c18e304715c224
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2846777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7351c3a5ca0286cd00681718bc54023b7a0b10bcdab11bdb304e1b17e787aaa5`

```dockerfile
```

-	Layers:
	-	`sha256:91509ebf0069fd05338aca22eb954d626ad7ea62f9c416b3cd7a3c35019eedbd`  
		Last Modified: Fri, 18 Apr 2025 18:37:43 GMT  
		Size: 2.8 MB (2829207 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:937f479a29f625f38168e1d89eaff1467cb099686de5a0c9d6c7ca8a79c12306`  
		Last Modified: Fri, 18 Apr 2025 18:37:43 GMT  
		Size: 17.6 KB (17570 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:25-ea-19-slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:efdce33ebb41a54b39e08445890cba79d0b1eebdd85589a867ca10aae5efbf1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.7 MB (240678198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:856ae066d52ef7a85fc162d388ab6267285c115f4aeae3c98bf53bcd4e0e3249`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 07 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1743984000'
# Fri, 18 Apr 2025 00:48:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 18 Apr 2025 00:48:12 GMT
ENV JAVA_HOME=/usr/local/openjdk-25
# Fri, 18 Apr 2025 00:48:12 GMT
ENV PATH=/usr/local/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 18 Apr 2025 00:48:12 GMT
ENV LANG=C.UTF-8
# Fri, 18 Apr 2025 00:48:12 GMT
ENV JAVA_VERSION=25-ea+19
# Fri, 18 Apr 2025 00:48:12 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/19/GPL/openjdk-25-ea+19_linux-x64_bin.tar.gz'; 			downloadSha256='5d10a87dcb2a162df9f7ab0c97cc77eff71c53ad442cbf40cce33b8ab6ab117a'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/19/GPL/openjdk-25-ea+19_linux-aarch64_bin.tar.gz'; 			downloadSha256='1324cfa105b4ce10e2ab854c20d7e1a4eda81fb6a1df35dacadc8d65b0b59351'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 18 Apr 2025 00:48:12 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:59627ca2e9712141a7d131bec6c9931f8ecea11eac34d96bd1213ccea68e18e5`  
		Last Modified: Tue, 08 Apr 2025 00:23:35 GMT  
		Size: 28.7 MB (28749498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:609a7e4368bd79410cad3a425c733de39f59e4e41157ea12172a4ef1e0bee0d9`  
		Last Modified: Mon, 14 Apr 2025 23:03:48 GMT  
		Size: 1.6 MB (1565936 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:126503289a8eee395f2409b45e62b0787455530145a9efc8e2e8dab9a074db85`  
		Last Modified: Fri, 18 Apr 2025 18:41:48 GMT  
		Size: 210.4 MB (210362764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-ea-19-slim-bullseye` - unknown; unknown

```console
$ docker pull openjdk@sha256:3f3b2fbe28748e719f5c9fce2554d7ab0a755c89d4b3cce8795608de8fac7393
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2846572 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b346764dab1cbe9ce6035b90bd574a964429fb71c10d3a316762a5466fe02ec4`

```dockerfile
```

-	Layers:
	-	`sha256:0e4e7ff97b12f580c183302c71eda2b541b7e46c90b02f86e91529aaec731e51`  
		Last Modified: Fri, 18 Apr 2025 18:41:43 GMT  
		Size: 2.8 MB (2828859 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6e675d76eb707a0da85d8fba6fae197b80a36d6928194ea898efd4e98aa7b39a`  
		Last Modified: Fri, 18 Apr 2025 18:41:43 GMT  
		Size: 17.7 KB (17713 bytes)  
		MIME: application/vnd.in-toto+json
