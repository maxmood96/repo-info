## `openjdk:27-ea-28-jdk-slim-bookworm`

```console
$ docker pull openjdk@sha256:53120dfaa2cbee524457b208cbd4cb4986cd73711106645b8030ae4281849ff4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:27-ea-28-jdk-slim-bookworm` - linux; amd64

```console
$ docker pull openjdk@sha256:3b80af49e036644bd29d294adac4d7f257b9f4557f41aca3e941c8cbd2591718
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **259.4 MB (259416221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3b1caa7da64cfe4352a66e36c860df27d55af9811ac00dbb4154e50769b14e9`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1782172800'
# Fri, 26 Jun 2026 17:49:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 26 Jun 2026 17:49:34 GMT
ENV JAVA_HOME=/usr/local/openjdk-27
# Fri, 26 Jun 2026 17:49:34 GMT
ENV PATH=/usr/local/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Jun 2026 17:49:34 GMT
ENV LANG=C.UTF-8
# Fri, 26 Jun 2026 17:49:34 GMT
ENV JAVA_VERSION=27-ea+28
# Fri, 26 Jun 2026 17:49:34 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/28/GPL/openjdk-27-ea+28_linux-x64_bin.tar.gz'; 			downloadSha256='45707add322e7be16c9eaf4e6f15febf5bd06baeab88aea73d3a89fae0d7bcd7'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/28/GPL/openjdk-27-ea+28_linux-aarch64_bin.tar.gz'; 			downloadSha256='1fe32bfb8b4a3533d1cbd2199cbdb9c62d72032b409da56d58135460a7e0c5a5'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 26 Jun 2026 17:49:34 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:68629629b516c3cd6f5e71ffbe18e32afb1ae5b4926c92d058c0f11ef1fd58a3`  
		Last Modified: Wed, 24 Jun 2026 00:27:52 GMT  
		Size: 28.2 MB (28237639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30232b034a56c89b1741b3515c090e303090394dd9f780cc14692d7b92d7b27b`  
		Last Modified: Fri, 26 Jun 2026 17:49:54 GMT  
		Size: 4.0 MB (4032877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a4e87405edf8085c6a6e180684990616fadf85aa947ac776d5e79627c8557fe`  
		Last Modified: Fri, 26 Jun 2026 17:49:58 GMT  
		Size: 227.1 MB (227145705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-28-jdk-slim-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:06a5e2a64e2113134c74fe5f907ba8d2f0c34d396929ae408b078fe244b28771
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2664160 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:477331f8974617d313ec40d9f9dfcdcffe0e786d283fc288c746f328489e78fc`

```dockerfile
```

-	Layers:
	-	`sha256:5fb13416cbe06c76e707c27fc385b55f0b985e5fd927ceee08f7282699e5a67f`  
		Last Modified: Fri, 26 Jun 2026 17:49:53 GMT  
		Size: 2.6 MB (2647290 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2ffe9161cde7f2db81209445c7e02c10fea05b4f97903974e58140cf88014844`  
		Last Modified: Fri, 26 Jun 2026 17:49:53 GMT  
		Size: 16.9 KB (16870 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:27-ea-28-jdk-slim-bookworm` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:075b03d83a0171872b9973488b4347a86e0e0dbc313af62406c5fbd7ec4c3821
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.1 MB (257091917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a9c3102bc424ca0e58ae09d2a185388f6f08b6d1cfc1796e3faf4f2028cdadc`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1782172800'
# Fri, 26 Jun 2026 17:54:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 26 Jun 2026 17:54:34 GMT
ENV JAVA_HOME=/usr/local/openjdk-27
# Fri, 26 Jun 2026 17:54:34 GMT
ENV PATH=/usr/local/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Jun 2026 17:54:34 GMT
ENV LANG=C.UTF-8
# Fri, 26 Jun 2026 17:54:34 GMT
ENV JAVA_VERSION=27-ea+28
# Fri, 26 Jun 2026 17:54:34 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/28/GPL/openjdk-27-ea+28_linux-x64_bin.tar.gz'; 			downloadSha256='45707add322e7be16c9eaf4e6f15febf5bd06baeab88aea73d3a89fae0d7bcd7'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/28/GPL/openjdk-27-ea+28_linux-aarch64_bin.tar.gz'; 			downloadSha256='1fe32bfb8b4a3533d1cbd2199cbdb9c62d72032b409da56d58135460a7e0c5a5'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 26 Jun 2026 17:54:34 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:74f1dcfcc9c80045f6f6394ffcfc261cb19d0c71b97e964aec3d4abf4e0f7009`  
		Last Modified: Wed, 24 Jun 2026 00:27:48 GMT  
		Size: 28.1 MB (28122418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a52bd1df62352558afc70c7680d21cd765cc6b9b6ca2073582002b56eac3679`  
		Last Modified: Fri, 26 Jun 2026 17:54:56 GMT  
		Size: 3.9 MB (3852802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b4e7e2bda7a8dc1d8cacee831a5ce9ae9b5b3337ad7d66af5e2ef3acffb070c`  
		Last Modified: Fri, 26 Jun 2026 17:55:00 GMT  
		Size: 225.1 MB (225116697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-28-jdk-slim-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:3caf0d1f634ec9ffe015465b979f12f429d5ebc71bb83820af2829bc80a9e623
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2663914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:914ab1452fb94ed7f89c29716967b77ae7c450b0451df919c3955578030222e8`

```dockerfile
```

-	Layers:
	-	`sha256:ebb5acc96faa6511ddc5d242b02b98d44404b77d0216a8dc0c575bc1cfb0eae0`  
		Last Modified: Fri, 26 Jun 2026 17:54:55 GMT  
		Size: 2.6 MB (2646924 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:01fda964ad5449a77bd5e12126233a1422c343d1a2b1ca7d72d5d6aa6ee1c1dc`  
		Last Modified: Fri, 26 Jun 2026 17:54:55 GMT  
		Size: 17.0 KB (16990 bytes)  
		MIME: application/vnd.in-toto+json
