## `openjdk:27-ea-14-trixie`

```console
$ docker pull openjdk@sha256:51894effbaf38ff1b20767f47817050e39032a6a948a4fca0160f83d2da70766
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:27-ea-14-trixie` - linux; amd64

```console
$ docker pull openjdk@sha256:76792a25dc14177e1ea5e95d509b2a6a5aa36cb4e317c7626a0ccf72ab8c0f71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **387.4 MB (387359421 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b27e0c60e5a9586d9416958884b11b6a5929d8e2757d1a66ec9d44f0a4c42a26`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 22:38:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Mon, 16 Mar 2026 23:25:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Mon, 23 Mar 2026 17:58:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 Mar 2026 17:58:41 GMT
ENV JAVA_HOME=/usr/local/openjdk-27
# Mon, 23 Mar 2026 17:58:41 GMT
ENV PATH=/usr/local/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 23 Mar 2026 17:58:41 GMT
ENV LANG=C.UTF-8
# Mon, 23 Mar 2026 17:58:41 GMT
ENV JAVA_VERSION=27-ea+14
# Mon, 23 Mar 2026 17:58:41 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/14/GPL/openjdk-27-ea+14_linux-x64_bin.tar.gz'; 			downloadSha256='64b478b9973d8d04e1680cdfaf11a8e93f8a17f962af3ddb1c61b76a62c0d699'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/14/GPL/openjdk-27-ea+14_linux-aarch64_bin.tar.gz'; 			downloadSha256='c99686ed0406f05a113b6467b6a57699864922c476481609a703c6dd91534f45'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Mon, 23 Mar 2026 17:58:41 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:8f6ad858d0a46fa8ee628532c70b8dc82d06179d543b0b09ec19fc03d4c5b373`  
		Last Modified: Mon, 16 Mar 2026 21:53:17 GMT  
		Size: 49.3 MB (49297530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b012eb15dff0bce418c03ec940325aee6aa4300d771c325728855697e620c63a`  
		Last Modified: Mon, 16 Mar 2026 22:38:25 GMT  
		Size: 25.6 MB (25621715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee3a0e7d77f0c84203cab438fcf345647c8121bbd80506a3c692f8608a14c4f4`  
		Last Modified: Mon, 16 Mar 2026 23:25:57 GMT  
		Size: 67.8 MB (67780758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9023fc82491b736b718e31df86a2900ad62b967477a30fe1ac3c9d610315f99`  
		Last Modified: Mon, 23 Mar 2026 17:59:06 GMT  
		Size: 16.1 MB (16063938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5059eb65b20f7f2da5908990f04634d207b82abb8329aeedab4f59b3ccd8f956`  
		Last Modified: Mon, 23 Mar 2026 17:59:10 GMT  
		Size: 228.6 MB (228595480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-14-trixie` - unknown; unknown

```console
$ docker pull openjdk@sha256:73cae5462c11dbc01df2a492f443d75cf447a66689e2fdcc5c3647dbfad09321
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.5 MB (8529049 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b52f622a972a281dda6fbc1c5897a48927559369574b2b9f4b21f36327afda46`

```dockerfile
```

-	Layers:
	-	`sha256:9c9444b865186ce88762df54fa0f60f6e2b7139d6b25b5db371363bad730b1e6`  
		Last Modified: Mon, 23 Mar 2026 17:59:06 GMT  
		Size: 8.5 MB (8511136 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:914635ce2ca9a4be3663ee8b4cb26f6837a98404b225a274129e47843fd89783`  
		Last Modified: Mon, 23 Mar 2026 17:59:05 GMT  
		Size: 17.9 KB (17913 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:27-ea-14-trixie` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:330b138162846585b6e377d3ea6747894f17f7cf008bb388bb0f0488c4d5cb8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **384.9 MB (384904882 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48db679a3abe6966981f5364f5fc709ba343837f764af32e2c1e952799b1b1a6`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 22:40:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Mon, 16 Mar 2026 23:30:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Mon, 23 Mar 2026 17:58:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 Mar 2026 17:58:34 GMT
ENV JAVA_HOME=/usr/local/openjdk-27
# Mon, 23 Mar 2026 17:58:34 GMT
ENV PATH=/usr/local/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 23 Mar 2026 17:58:34 GMT
ENV LANG=C.UTF-8
# Mon, 23 Mar 2026 17:58:34 GMT
ENV JAVA_VERSION=27-ea+14
# Mon, 23 Mar 2026 17:58:34 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/14/GPL/openjdk-27-ea+14_linux-x64_bin.tar.gz'; 			downloadSha256='64b478b9973d8d04e1680cdfaf11a8e93f8a17f962af3ddb1c61b76a62c0d699'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/14/GPL/openjdk-27-ea+14_linux-aarch64_bin.tar.gz'; 			downloadSha256='c99686ed0406f05a113b6467b6a57699864922c476481609a703c6dd91534f45'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Mon, 23 Mar 2026 17:58:34 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:deab8db42772fcfeb45003461fe0eb7bf63bdb29199a4fb76242b9493437c28b`  
		Last Modified: Mon, 16 Mar 2026 21:53:03 GMT  
		Size: 49.7 MB (49664953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6778b62bd97b31237948877e89abc29ad2b2c003f3b965027457c8c90d4f44e0`  
		Last Modified: Mon, 16 Mar 2026 22:40:45 GMT  
		Size: 25.0 MB (25023728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d16813bdedcf0a1acbd78336c5bed6fbfaee2674574408140ba7e896cd49cb95`  
		Last Modified: Mon, 16 Mar 2026 23:31:00 GMT  
		Size: 67.6 MB (67584568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b39cc3e155d5fb15c647a926a179dcb5adac50c7cbf4c6cbe9881a744ff51f7`  
		Last Modified: Mon, 23 Mar 2026 17:59:00 GMT  
		Size: 16.1 MB (16071531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b48a150511aae41d47d5d4ac912a79e783e11b2c6cfc8b8974491ef4a041b3a3`  
		Last Modified: Mon, 23 Mar 2026 17:59:04 GMT  
		Size: 226.6 MB (226560102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-14-trixie` - unknown; unknown

```console
$ docker pull openjdk@sha256:997b17288ecf52b9f6c9fd21d7ceaf58597884d5a85a3a2ad9332a6b112a7780
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 MB (8723958 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89ddb1ee8285cb499f3518b70f41690300f3c77f8946db9d4f087a6a75dd95ca`

```dockerfile
```

-	Layers:
	-	`sha256:3a78f4e039a89720127bad3d1367e78f01ea4cddcfd6cc1fe615638b9f82bbf3`  
		Last Modified: Mon, 23 Mar 2026 17:58:59 GMT  
		Size: 8.7 MB (8705926 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dd50a8a2acd5be8ee235b3b50a5d6e8841cf2d4490d6c2e5e5f1c6d8affec827`  
		Last Modified: Mon, 23 Mar 2026 17:58:59 GMT  
		Size: 18.0 KB (18032 bytes)  
		MIME: application/vnd.in-toto+json
