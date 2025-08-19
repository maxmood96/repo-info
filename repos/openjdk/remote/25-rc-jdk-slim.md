## `openjdk:25-rc-jdk-slim`

```console
$ docker pull openjdk@sha256:21f70fe5abab9828c5bfd7eea60459b3881c21846e20d9798f5ae18fc62d3b92
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:25-rc-jdk-slim` - linux; amd64

```console
$ docker pull openjdk@sha256:e4a9bf84350abd4a539be3f2c2df35c695fbeafe43eac2310ef0696f7fbb83ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.4 MB (255380543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ade42db5fb468991ca9bfd34c1350fcc58cf8aa70b730e723326439d4d1195bc`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1754870400'
# Sat, 16 Aug 2025 00:48:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 16 Aug 2025 00:48:25 GMT
ENV JAVA_HOME=/usr/local/openjdk-25
# Sat, 16 Aug 2025 00:48:25 GMT
ENV PATH=/usr/local/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 16 Aug 2025 00:48:25 GMT
ENV LANG=C.UTF-8
# Sat, 16 Aug 2025 00:48:25 GMT
ENV JAVA_VERSION=25
# Sat, 16 Aug 2025 00:48:25 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/GA/jdk25/bd75d5f9689641da8e1daabeccb5528b/36/GPL/openjdk-25_linux-x64_bin.tar.gz'; 			downloadSha256='59cdcaf255add4721de38eb411d4ecfe779356b61fb671aee63c7dec78054c2b'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/GA/jdk25/bd75d5f9689641da8e1daabeccb5528b/36/GPL/openjdk-25_linux-aarch64_bin.tar.gz'; 			downloadSha256='f4a8d27429458a529148f90ebafcd1ae9b1968fa323f9e5e40d579a5c8c0288f'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 16 Aug 2025 00:48:25 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:396b1da7636e2dcd10565cb4f2f952cbb4a8a38b58d3b86a2cacb172fb70117c`  
		Last Modified: Tue, 12 Aug 2025 20:45:08 GMT  
		Size: 29.8 MB (29773285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:984cebfe1ad4fde30aec811f18a3a781cbefaf502d1bad4efce6aff719a145c4`  
		Last Modified: Mon, 18 Aug 2025 18:16:37 GMT  
		Size: 2.4 MB (2371057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a919f796dfe50ef7faa8f0655f5dd030a870a369a8429860477fb9a68404fb1f`  
		Last Modified: Mon, 18 Aug 2025 21:32:56 GMT  
		Size: 223.2 MB (223236201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-rc-jdk-slim` - unknown; unknown

```console
$ docker pull openjdk@sha256:84e94f8c1190c4448f3977edeb23789edc7c00346098a200ca9e6e216340ef08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2299150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2d4276860d90d0503b8a65cda00e2cfa286ef629ea5019bb8174eff0ad5fb6c`

```dockerfile
```

-	Layers:
	-	`sha256:028c362174e3d8ea4ca832f063efae1508a5ce06665c936fcf7b5dcfa530149e`  
		Last Modified: Mon, 18 Aug 2025 21:23:47 GMT  
		Size: 2.3 MB (2280974 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5a9b573fdae1342122b545127c4950f60754cd03a32857d966a08015c2694076`  
		Last Modified: Mon, 18 Aug 2025 21:23:48 GMT  
		Size: 18.2 KB (18176 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:25-rc-jdk-slim` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:0a94cc713ca4f022e99b2c06db11e945d4b2c52a8865e7e975a3219bb4cc9b66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.5 MB (253483328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d8951f3a090b569cc02bf61867fa28f974cc9f7811941bb1630192ec7794d17`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1754870400'
# Sat, 16 Aug 2025 00:48:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 16 Aug 2025 00:48:25 GMT
ENV JAVA_HOME=/usr/local/openjdk-25
# Sat, 16 Aug 2025 00:48:25 GMT
ENV PATH=/usr/local/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 16 Aug 2025 00:48:25 GMT
ENV LANG=C.UTF-8
# Sat, 16 Aug 2025 00:48:25 GMT
ENV JAVA_VERSION=25
# Sat, 16 Aug 2025 00:48:25 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/GA/jdk25/bd75d5f9689641da8e1daabeccb5528b/36/GPL/openjdk-25_linux-x64_bin.tar.gz'; 			downloadSha256='59cdcaf255add4721de38eb411d4ecfe779356b61fb671aee63c7dec78054c2b'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/GA/jdk25/bd75d5f9689641da8e1daabeccb5528b/36/GPL/openjdk-25_linux-aarch64_bin.tar.gz'; 			downloadSha256='f4a8d27429458a529148f90ebafcd1ae9b1968fa323f9e5e40d579a5c8c0288f'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 16 Aug 2025 00:48:25 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:9a6263cdeaa5d408640880103ee36920ef814974ca8e2674412ad6460e8968c9`  
		Last Modified: Tue, 12 Aug 2025 22:12:42 GMT  
		Size: 30.1 MB (30136044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8aafae0cffde53a4a97b3a67ecda78936d66918ef646e27519a1c2c6551a203`  
		Last Modified: Mon, 18 Aug 2025 22:23:58 GMT  
		Size: 2.3 MB (2314286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f06aa8fe7b1dffc4ae54314fdc9107c867c2784f90166bcc799b4d2f5fa50f63`  
		Last Modified: Tue, 19 Aug 2025 00:44:15 GMT  
		Size: 221.0 MB (221032998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-rc-jdk-slim` - unknown; unknown

```console
$ docker pull openjdk@sha256:e1d26e36bb902b0e33f1c432182b5fbd7972b5390f2f073a45dd67c587ece7d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2299003 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0446725be3c4811e7a9f19acc284a6f771aef76c46e369465326eada8806b6f`

```dockerfile
```

-	Layers:
	-	`sha256:002fb0ce5f13ef0cf522fcd7f3e82244dd72739792976c4b5303af86ebc55d7a`  
		Last Modified: Tue, 19 Aug 2025 00:23:47 GMT  
		Size: 2.3 MB (2280660 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:31bd1cce61a655ba5b382df82a66ff1f3ec6c0acd6788f41b28029a5ddfc7792`  
		Last Modified: Tue, 19 Aug 2025 00:23:48 GMT  
		Size: 18.3 KB (18343 bytes)  
		MIME: application/vnd.in-toto+json
