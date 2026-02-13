## `openjdk:26-rc-jdk-bookworm`

```console
$ docker pull openjdk@sha256:0570c615091e08ae5811dd6ad43f545924a31ba882ecf993eaa4faca9c8796a4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:26-rc-jdk-bookworm` - linux; amd64

```console
$ docker pull openjdk@sha256:16a1b9fa808df5dcca49dd127e6c97c6473ba64e50d4791ce53dac7631c017b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **381.8 MB (381845988 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e98c7e32a5ada14db605eff300a3b5ba0b1dad7870bc44cc4a28d2553c80384`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 02:41:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 03:28:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 13 Feb 2026 00:00:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 13 Feb 2026 00:00:15 GMT
ENV JAVA_HOME=/usr/local/openjdk-26
# Fri, 13 Feb 2026 00:00:15 GMT
ENV PATH=/usr/local/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 13 Feb 2026 00:00:15 GMT
ENV LANG=C.UTF-8
# Fri, 13 Feb 2026 00:00:15 GMT
ENV JAVA_VERSION=26
# Fri, 13 Feb 2026 00:00:15 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/GA/jdk26/c3cc523845074aa0af4f5e1e1ed4151d/34/GPL/openjdk-26_linux-x64_bin.tar.gz'; 			downloadSha256='e7c907ec1036e5480609f8212e6f1e7f710310e029d097e4e1a9645c43676945'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/GA/jdk26/c3cc523845074aa0af4f5e1e1ed4151d/34/GPL/openjdk-26_linux-aarch64_bin.tar.gz'; 			downloadSha256='aeb9ccc00550a012197834334a9a6cbc03e7938774fcaf59dfa7ed158b66465f'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 13 Feb 2026 00:00:15 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:6bc9f599b3efabc64230fd3b969d7654fcd6c6c98ad7cf7470093fe85274a7fc`  
		Last Modified: Tue, 03 Feb 2026 01:13:20 GMT  
		Size: 48.5 MB (48481483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89edcaae7ec479668d9bf0891145726173a305c809a8c4165723ceaf15b5a05f`  
		Last Modified: Tue, 03 Feb 2026 02:41:49 GMT  
		Size: 24.0 MB (24038446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbceb003542957cee7df7b79249eaf0a71d21c5203d086969b565fb6dec85d86`  
		Last Modified: Tue, 03 Feb 2026 03:28:33 GMT  
		Size: 64.4 MB (64395971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5bee55a013cc166e058ac2d8f7b285d7abc2e24098a25c608551b594f9280c4`  
		Last Modified: Fri, 13 Feb 2026 00:00:38 GMT  
		Size: 16.9 MB (16944800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:725dc3c6135ad46a11c24d8f5ce26347cda3ce7a25b1f84738bce8986594d5a6`  
		Last Modified: Fri, 13 Feb 2026 00:00:44 GMT  
		Size: 228.0 MB (227985288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-rc-jdk-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:bb93d90a5c516dc5ae95c2f9c20435fc234ddae167fd25ba0155cb9de6a37a51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 MB (8685565 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0572298e7cbec3b88002f71d312cfd8cdf1f47f291a8564b9e435a5d458aca1`

```dockerfile
```

-	Layers:
	-	`sha256:995c77f97537b32c209be4bb3386d4a19af3a7bf7bb59c8d3a2adecd4b6946d2`  
		Last Modified: Fri, 13 Feb 2026 00:00:38 GMT  
		Size: 8.7 MB (8668215 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b190338c0cad7e5ef0a402fc97a18cb2f8e217b5ce31b8803782b271ce537e0b`  
		Last Modified: Fri, 13 Feb 2026 00:00:40 GMT  
		Size: 17.4 KB (17350 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:26-rc-jdk-bookworm` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:ff3ab37b927fa21f6a07e10ae744dde896b9ef1ec32e9d30ff06a5f5a312ed0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **380.1 MB (380079766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8dcc2a3fd038a5d4cf978d653bad2d769311e267c8d845dc26ba2d6af75ac13a`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 02:44:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 03:46:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 13 Feb 2026 00:02:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 13 Feb 2026 00:02:15 GMT
ENV JAVA_HOME=/usr/local/openjdk-26
# Fri, 13 Feb 2026 00:02:15 GMT
ENV PATH=/usr/local/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 13 Feb 2026 00:02:15 GMT
ENV LANG=C.UTF-8
# Fri, 13 Feb 2026 00:02:15 GMT
ENV JAVA_VERSION=26
# Fri, 13 Feb 2026 00:02:15 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/GA/jdk26/c3cc523845074aa0af4f5e1e1ed4151d/34/GPL/openjdk-26_linux-x64_bin.tar.gz'; 			downloadSha256='e7c907ec1036e5480609f8212e6f1e7f710310e029d097e4e1a9645c43676945'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/GA/jdk26/c3cc523845074aa0af4f5e1e1ed4151d/34/GPL/openjdk-26_linux-aarch64_bin.tar.gz'; 			downloadSha256='aeb9ccc00550a012197834334a9a6cbc03e7938774fcaf59dfa7ed158b66465f'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 13 Feb 2026 00:02:15 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:64e8f4c09e7ac936ecc3deb0e61613f653224c28b2e35fa9d8e6e11cbdb5f911`  
		Last Modified: Tue, 03 Feb 2026 01:13:22 GMT  
		Size: 48.4 MB (48365956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:404413e6e45accf116074dace885c7ccf2917479ae04f2f46c046b6ae1909254`  
		Last Modified: Tue, 03 Feb 2026 02:44:54 GMT  
		Size: 23.6 MB (23604842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1e9aa4982c2a67e202ea283fc3760e94d8d8b16966c616e01ad0238abbaac82`  
		Last Modified: Tue, 03 Feb 2026 03:46:50 GMT  
		Size: 64.5 MB (64479687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41784bcf866b53ed969c438839a9fa3ed9bca7b5ac9de1f1e3a8ca743f53132a`  
		Last Modified: Fri, 13 Feb 2026 00:02:41 GMT  
		Size: 17.7 MB (17728538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07ca442ba39b19bbc19c3001e933daf94bb98449de1dcddf65d0b3bdb41e4acc`  
		Last Modified: Fri, 13 Feb 2026 00:02:45 GMT  
		Size: 225.9 MB (225900743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-rc-jdk-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:ab5d55f8f1f902ed752db222d2933ac0b03a4347d8d091c3148716d353333cdd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8822482 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7069f1fe06ce764a7bb37567761c58df7ab2cb83b69d836ca45e0e7fd2a9894`

```dockerfile
```

-	Layers:
	-	`sha256:19d6c04a1568d3e4b5ca0cef924f56b5e20b496bcc0bc7fa4c71ca39433e33d1`  
		Last Modified: Fri, 13 Feb 2026 00:02:41 GMT  
		Size: 8.8 MB (8805036 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:987d92629450c8ab4cd75157e7d711580bb664d3b51c2857f3e65941246885c9`  
		Last Modified: Fri, 13 Feb 2026 00:02:40 GMT  
		Size: 17.4 KB (17446 bytes)  
		MIME: application/vnd.in-toto+json
