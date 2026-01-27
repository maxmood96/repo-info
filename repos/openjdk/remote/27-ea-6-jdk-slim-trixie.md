## `openjdk:27-ea-6-jdk-slim-trixie`

```console
$ docker pull openjdk@sha256:e845b70a966d9f2cfd17b19ff6d07401f35266f231b8890dd36ce99726f38188
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:27-ea-6-jdk-slim-trixie` - linux; amd64

```console
$ docker pull openjdk@sha256:1d31174c1d2b17cdbabec0e9857a87fd9041746758f675d500a9184d92838a6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **260.5 MB (260536494 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70f1d1928182da6e163d18d27c744832c53c0a54c93154b952cb69119faada50`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1768176000'
# Mon, 26 Jan 2026 22:11:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 26 Jan 2026 22:12:03 GMT
ENV JAVA_HOME=/usr/local/openjdk-27
# Mon, 26 Jan 2026 22:12:03 GMT
ENV PATH=/usr/local/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 26 Jan 2026 22:12:03 GMT
ENV LANG=C.UTF-8
# Mon, 26 Jan 2026 22:12:03 GMT
ENV JAVA_VERSION=27-ea+6
# Mon, 26 Jan 2026 22:12:03 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/6/GPL/openjdk-27-ea+6_linux-x64_bin.tar.gz'; 			downloadSha256='394c8962532cfeb8e27701615449f453f090145d33f7d24947aa6ceed07dcce6'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/6/GPL/openjdk-27-ea+6_linux-aarch64_bin.tar.gz'; 			downloadSha256='e516f107cd78b8abf3500494b93d20718e0779fa79a12399f30928c615593789'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Mon, 26 Jan 2026 22:12:03 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:119d43eec815e5f9a47da3a7d59454581b1e204b0c34db86f171b7ceb3336533`  
		Last Modified: Tue, 13 Jan 2026 00:42:27 GMT  
		Size: 29.8 MB (29773685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:471d0996426a5e6174b85f639cab10e45451bdc56114ab56763d4d126727a06c`  
		Last Modified: Mon, 26 Jan 2026 22:12:22 GMT  
		Size: 2.4 MB (2371037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c688648fbb3fb91806f9ff4729844d85c3649ee101c4976efe009e8391e7667f`  
		Last Modified: Mon, 26 Jan 2026 22:12:27 GMT  
		Size: 228.4 MB (228391772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-6-jdk-slim-trixie` - unknown; unknown

```console
$ docker pull openjdk@sha256:6a47a8986c75fd53d3f3893f7c2bde8679048a0e0d9807303fa4c46dd8292401
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2296927 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d3177b0a27b42cdf9b883409295a39ea69df4d35f071855227486512b53c1f0`

```dockerfile
```

-	Layers:
	-	`sha256:866e1058ae4fc6558486cb33c72dc235f5e5906a0ad7b5a89c952671d4354ee0`  
		Last Modified: Mon, 26 Jan 2026 22:12:22 GMT  
		Size: 2.3 MB (2278839 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:67c10dbe5af0c5255826cb40fc4851350b48792c513bc6d8dc97628debd433a0`  
		Last Modified: Mon, 26 Jan 2026 22:12:22 GMT  
		Size: 18.1 KB (18088 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:27-ea-6-jdk-slim-trixie` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:f043622e7cc6515a03f98ba78ba053034fecfd8e86f8215d151178bf649f65a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.8 MB (258759546 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a8dfbc4648e2cbf98e6453102b354491006162c24e619e2a9854d64d1eb241f`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1768176000'
# Mon, 26 Jan 2026 22:10:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 26 Jan 2026 22:11:11 GMT
ENV JAVA_HOME=/usr/local/openjdk-27
# Mon, 26 Jan 2026 22:11:11 GMT
ENV PATH=/usr/local/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 26 Jan 2026 22:11:11 GMT
ENV LANG=C.UTF-8
# Mon, 26 Jan 2026 22:11:11 GMT
ENV JAVA_VERSION=27-ea+6
# Mon, 26 Jan 2026 22:11:11 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/6/GPL/openjdk-27-ea+6_linux-x64_bin.tar.gz'; 			downloadSha256='394c8962532cfeb8e27701615449f453f090145d33f7d24947aa6ceed07dcce6'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/6/GPL/openjdk-27-ea+6_linux-aarch64_bin.tar.gz'; 			downloadSha256='e516f107cd78b8abf3500494b93d20718e0779fa79a12399f30928c615593789'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Mon, 26 Jan 2026 22:11:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:d637807aba98f742a62ad9b0146579ceb0297a3c831f56b2361664b7f5fbc75b`  
		Last Modified: Tue, 13 Jan 2026 00:42:41 GMT  
		Size: 30.1 MB (30134042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50b53334d2bcac8bc59e10ddf508c49aef1fb810859e81fbeb2a76d2563364ee`  
		Last Modified: Mon, 26 Jan 2026 22:11:32 GMT  
		Size: 2.3 MB (2314170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce43e0d3f575ec8374718300ab8480b2a869de079b19e8a52cda4294edf782eb`  
		Last Modified: Mon, 26 Jan 2026 22:11:36 GMT  
		Size: 226.3 MB (226311334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-6-jdk-slim-trixie` - unknown; unknown

```console
$ docker pull openjdk@sha256:006ff1a9003d906bded96b76ee280a440d0ab41c57dc330c4852c73deda48e50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2296780 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d22603715a5caa51735a4d5fe89f13f87ebc10c8a75ba5fae4e3ed4df64549af`

```dockerfile
```

-	Layers:
	-	`sha256:bc7d0da0cdb7dfc9bee04a13e9832e36b2757fd874c4f4abfbe043a8add14406`  
		Last Modified: Mon, 26 Jan 2026 22:11:32 GMT  
		Size: 2.3 MB (2278525 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:91c66ed9faa0c3bf51b7fa118803c6df3d20d40c1e7a999e29cd9ebcddf4c367`  
		Last Modified: Mon, 26 Jan 2026 22:11:32 GMT  
		Size: 18.3 KB (18255 bytes)  
		MIME: application/vnd.in-toto+json
