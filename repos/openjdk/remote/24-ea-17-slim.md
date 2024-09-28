## `openjdk:24-ea-17-slim`

```console
$ docker pull openjdk@sha256:d84e5801fdb5f2fec03a6e84a538f7f6bd4ed0ba8834ef7e26c214f17668668f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `openjdk:24-ea-17-slim` - linux; amd64

```console
$ docker pull openjdk@sha256:7fe4b436108ba9761c6b64e48867c4bb953562a42cfcd546993ce1e5f0771970
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **245.5 MB (245450918 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f0e3b050a24fb143d997fec6a1e8774e359e3a802ebbb40a01cc774315940d2`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 27 Sep 2024 04:29:32 GMT
ADD file:a9a95cfab16803be03e59ade41622ef5061cf90f2d034304fe4ac1ee9ff30389 in / 
# Fri, 27 Sep 2024 04:29:32 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 06:48:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 27 Sep 2024 06:48:27 GMT
ENV JAVA_HOME=/usr/local/openjdk-24
# Fri, 27 Sep 2024 06:48:27 GMT
ENV PATH=/usr/local/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 27 Sep 2024 06:48:27 GMT
ENV LANG=C.UTF-8
# Fri, 27 Sep 2024 06:48:27 GMT
ENV JAVA_VERSION=24-ea+17
# Fri, 27 Sep 2024 06:48:27 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/17/GPL/openjdk-24-ea+17_linux-x64_bin.tar.gz'; 			downloadSha256='983faf25eff38b5b396afabd191a91b239a1d803a0dadd01863861ecf731f034'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/17/GPL/openjdk-24-ea+17_linux-aarch64_bin.tar.gz'; 			downloadSha256='c9eb980b4f1fde9c2387e0fab6b91b6f68cb109e3ddd43eda0013d9ee345f2dc'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 27 Sep 2024 06:48:27 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:302e3ee498053a7b5332ac79e8efebec16e900289fc1ecd1c754ce8fa047fcab`  
		Last Modified: Fri, 27 Sep 2024 04:33:11 GMT  
		Size: 29.1 MB (29126276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50d15fdc36e94775f8513d5ece51d2cc6fa391e696e8b7fbbcb587a14c5febd4`  
		Last Modified: Sat, 28 Sep 2024 01:01:03 GMT  
		Size: 4.0 MB (4017997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:564eb122b1c4a756de1a583f485e5cd875b32864fc01d5c86e792a4df7845553`  
		Last Modified: Sat, 28 Sep 2024 01:01:06 GMT  
		Size: 212.3 MB (212306645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-ea-17-slim` - unknown; unknown

```console
$ docker pull openjdk@sha256:40b8b17e64509aa97be4512775aa2aa5d7e18f039b3cfec1ba4635e2e69acda8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2523121 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:386a7a9635b0b489f7b07dd86ed650c9dfe62b8f57dd6cad24c1f66092b93154`

```dockerfile
```

-	Layers:
	-	`sha256:9b9afce0dd4956e3e63864e85c836fe051498701acde03d6a2563bb2416b777b`  
		Last Modified: Sat, 28 Sep 2024 01:01:03 GMT  
		Size: 2.5 MB (2503891 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1f73e638dd27b5c318152475c3be086c2c81056b35c4e41a206613f90464a993`  
		Last Modified: Sat, 28 Sep 2024 01:01:03 GMT  
		Size: 19.2 KB (19230 bytes)  
		MIME: application/vnd.in-toto+json
