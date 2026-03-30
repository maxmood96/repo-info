## `openjdk:27-ea-15-slim-bookworm`

```console
$ docker pull openjdk@sha256:5fcdb6f7f7686439f2cf718c74bf974319852b99334890e8dbcace032a898fde
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:27-ea-15-slim-bookworm` - linux; amd64

```console
$ docker pull openjdk@sha256:6b8107b6f3378670493d64ad6648762c56938fc66735d8cc2c7fc79305b2a6e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **260.9 MB (260924700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e309d301c8cd419d9d653b8385dfc76527661d7b86f1c62bbc1fc34b5a151b5f`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1773619200'
# Mon, 30 Mar 2026 17:52:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 30 Mar 2026 17:52:50 GMT
ENV JAVA_HOME=/usr/local/openjdk-27
# Mon, 30 Mar 2026 17:52:50 GMT
ENV PATH=/usr/local/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 30 Mar 2026 17:52:50 GMT
ENV LANG=C.UTF-8
# Mon, 30 Mar 2026 17:52:50 GMT
ENV JAVA_VERSION=27-ea+15
# Mon, 30 Mar 2026 17:52:50 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/15/GPL/openjdk-27-ea+15_linux-x64_bin.tar.gz'; 			downloadSha256='5cfe1cf2f5d5ebbcdd826c7298fbabc42d656edbe9544c74b1ee84df6e5326a7'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/15/GPL/openjdk-27-ea+15_linux-aarch64_bin.tar.gz'; 			downloadSha256='ab3f14d81c06590facec1138b71b55a7f64d47c0e0845113c9a8ecd4be6751bb'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Mon, 30 Mar 2026 17:52:50 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:6db0909c4473287ed4d1f950d26b8bc5b7b4206d365a0e7740cb89e46979153e`  
		Last Modified: Mon, 16 Mar 2026 21:52:32 GMT  
		Size: 28.2 MB (28236225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fc77a72f1bdbbc44bbf8397be6c927cbc1a7a64388dbae157a1c4a7f886bd33`  
		Last Modified: Mon, 30 Mar 2026 17:53:10 GMT  
		Size: 4.0 MB (4029208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73b1ba114cc2e8a033666c0c562073e6c1efa25df9a26ad4bab20c6283762684`  
		Last Modified: Mon, 30 Mar 2026 17:53:15 GMT  
		Size: 228.7 MB (228659267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-15-slim-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:1723a993d0c80ae798829eb3768f34f8d53b094aa239a332aeca2d8950f47c17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2666678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:761823a7f37047a5967c1b2e30f86a168aadcadc8e3b7d81e1ff2a2fb93143ed`

```dockerfile
```

-	Layers:
	-	`sha256:fd9f9f4a21c40308fad791144110dd27eae204fba65d70ff3f720dfe564202c1`  
		Last Modified: Mon, 30 Mar 2026 17:53:10 GMT  
		Size: 2.6 MB (2649807 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9f65f30b67f48d583a9514facc6051d7e88beb3c31613542bcfcb3e74d4fb39d`  
		Last Modified: Mon, 30 Mar 2026 17:53:10 GMT  
		Size: 16.9 KB (16871 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:27-ea-15-slim-bookworm` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:6382ef2d7420c04fd8c3a4ba63aa02b7676dd895de26fc4c817a39725656630a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.6 MB (258590695 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9810893bd83e0929cd4753bc3bb2b9733397448b78b400a1199e82a78c3df09`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1773619200'
# Mon, 30 Mar 2026 17:49:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 30 Mar 2026 17:49:27 GMT
ENV JAVA_HOME=/usr/local/openjdk-27
# Mon, 30 Mar 2026 17:49:27 GMT
ENV PATH=/usr/local/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 30 Mar 2026 17:49:27 GMT
ENV LANG=C.UTF-8
# Mon, 30 Mar 2026 17:49:27 GMT
ENV JAVA_VERSION=27-ea+15
# Mon, 30 Mar 2026 17:49:27 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/15/GPL/openjdk-27-ea+15_linux-x64_bin.tar.gz'; 			downloadSha256='5cfe1cf2f5d5ebbcdd826c7298fbabc42d656edbe9544c74b1ee84df6e5326a7'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/15/GPL/openjdk-27-ea+15_linux-aarch64_bin.tar.gz'; 			downloadSha256='ab3f14d81c06590facec1138b71b55a7f64d47c0e0845113c9a8ecd4be6751bb'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Mon, 30 Mar 2026 17:49:27 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:d997cc310c981ac52155d0d9fe28888b261a7746a3877bb0ca848fd1a83d319a`  
		Last Modified: Mon, 16 Mar 2026 21:53:12 GMT  
		Size: 28.1 MB (28116065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:724ca09b5ee71368753d9f3c8d595d237dab6fd5f3205921ec2e38f6224c4efa`  
		Last Modified: Mon, 30 Mar 2026 17:49:48 GMT  
		Size: 3.9 MB (3852007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93fdbf35bc12afe2891f6fb745ac87258eec3330b5f44dbb08550fbad0ad1e75`  
		Last Modified: Mon, 30 Mar 2026 17:49:53 GMT  
		Size: 226.6 MB (226622623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-15-slim-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:98194cccc51bdb68e54c4cea7ac01065e2ead49ec5b48c4c56c0689267c7a920
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2666431 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f11b6f1259061408fbd12d94a8377cedc1463a4af28cc095562316c9c536821f`

```dockerfile
```

-	Layers:
	-	`sha256:f9e900ce3e60fcfa648d4669d6e914a8118fe47fdf9527b5f80246f92756c5cb`  
		Last Modified: Mon, 30 Mar 2026 17:49:48 GMT  
		Size: 2.6 MB (2649441 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:10f87a1d57d1645eeb69366bd618141bc3b9f74bb6d76a533f90de1e4bad2d5c`  
		Last Modified: Mon, 30 Mar 2026 17:49:48 GMT  
		Size: 17.0 KB (16990 bytes)  
		MIME: application/vnd.in-toto+json
