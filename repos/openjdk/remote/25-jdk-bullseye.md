## `openjdk:25-jdk-bullseye`

```console
$ docker pull openjdk@sha256:62d7355700500b861bebc90dd2bacf492da2e456514f2e58686888cb7e65b54c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:25-jdk-bullseye` - linux; amd64

```console
$ docker pull openjdk@sha256:963ee1e68b4f5e8511bead769fb07065fe9a9ae27f554f8bb2b42a6e66ef7fb4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **361.1 MB (361065213 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1fca81a4ebf79d595e1a810787744d5221ad979cf3148ed55dda699468d27ac`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1747699200'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 30 May 2025 06:48:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 30 May 2025 06:48:10 GMT
ENV JAVA_HOME=/usr/local/openjdk-25
# Fri, 30 May 2025 06:48:10 GMT
ENV PATH=/usr/local/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 30 May 2025 06:48:10 GMT
ENV LANG=C.UTF-8
# Fri, 30 May 2025 06:48:10 GMT
ENV JAVA_VERSION=25-ea+25
# Fri, 30 May 2025 06:48:10 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/25/GPL/openjdk-25-ea+25_linux-x64_bin.tar.gz'; 			downloadSha256='bc7d25b610ced7056d3985b35440337c5dd07818d8929a0dc247b7b3669712d8'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/25/GPL/openjdk-25-ea+25_linux-aarch64_bin.tar.gz'; 			downloadSha256='3c4453d1cb4eafc8899b51154215251d72b551482710d30ae725e70012b311fc'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 30 May 2025 06:48:10 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:54107f2de180b7b6e9f909d2f1c6c18e10c700a6bd80a035d931768b06bb2905`  
		Last Modified: Tue, 03 Jun 2025 13:30:17 GMT  
		Size: 53.8 MB (53750195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06b6c820e694a6c19c297492ef4009391c7dfc83ecae735895f31a89e78b31fc`  
		Last Modified: Tue, 03 Jun 2025 13:30:14 GMT  
		Size: 15.8 MB (15764874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a69a02035012d2783a66ac7ecc549af09c1718d81affa5f9c39abcf969da971`  
		Last Modified: Tue, 03 Jun 2025 13:30:17 GMT  
		Size: 54.8 MB (54757308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0f8a12504a69c39f6b4624967833e156a8770914ea63aefe843a3d98fec5b31`  
		Last Modified: Tue, 03 Jun 2025 15:30:57 GMT  
		Size: 14.1 MB (14073014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4034e47af77cfec0962ee28100409694e745e7e090e2910d93d23ab245278009`  
		Last Modified: Tue, 03 Jun 2025 15:31:16 GMT  
		Size: 222.7 MB (222719822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-jdk-bullseye` - unknown; unknown

```console
$ docker pull openjdk@sha256:31c24133ad3faf8cbb21caa6bc3993795008fbedeffbf8a13da4902fd26d8da1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.4 MB (8422203 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb01481eaca4b8ad0366b093e7fb641c66ceab918a8b20f55ebcda8310d374ad`

```dockerfile
```

-	Layers:
	-	`sha256:3bfd6afb4b564ef6583619c6ca52b10acdc9b578c47e44663232c8b6dd7fabda`  
		Last Modified: Fri, 30 May 2025 17:37:43 GMT  
		Size: 8.4 MB (8403585 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7bc268555dc6fac58a199d951d0245c6ad3f2d6f651a5caff2e0997f1ee34d0a`  
		Last Modified: Fri, 30 May 2025 17:37:42 GMT  
		Size: 18.6 KB (18618 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:25-jdk-bullseye` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:482865c07899c46372c5c26efc6a3414765803917375b5eb20cf32ad94c8b75d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **358.9 MB (358882209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7bcffd57ba483696d9f8d143415d566a483ba5157a3729eacfda3b1800ff96af`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1747699200'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 30 May 2025 06:48:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 30 May 2025 06:48:10 GMT
ENV JAVA_HOME=/usr/local/openjdk-25
# Fri, 30 May 2025 06:48:10 GMT
ENV PATH=/usr/local/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 30 May 2025 06:48:10 GMT
ENV LANG=C.UTF-8
# Fri, 30 May 2025 06:48:10 GMT
ENV JAVA_VERSION=25-ea+25
# Fri, 30 May 2025 06:48:10 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/25/GPL/openjdk-25-ea+25_linux-x64_bin.tar.gz'; 			downloadSha256='bc7d25b610ced7056d3985b35440337c5dd07818d8929a0dc247b7b3669712d8'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/25/GPL/openjdk-25-ea+25_linux-aarch64_bin.tar.gz'; 			downloadSha256='3c4453d1cb4eafc8899b51154215251d72b551482710d30ae725e70012b311fc'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 30 May 2025 06:48:10 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:b2737025fe8da5b868f566cb4e3dc3330028cee06c83db854f56467eca6e09b8`  
		Last Modified: Tue, 03 Jun 2025 13:30:20 GMT  
		Size: 52.2 MB (52247755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a602f78cf8d696db9521d18affb7ecdb79ff690533efae26e3bdb1544cb1752`  
		Last Modified: Tue, 03 Jun 2025 13:31:09 GMT  
		Size: 15.8 MB (15750382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98c1b27af19f7550ac0d9c38bf6bcf26ba7eb53984e7e5e0886342816133c76e`  
		Last Modified: Tue, 03 Jun 2025 13:30:17 GMT  
		Size: 54.9 MB (54853236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9136a0327a59728e8bc997b12a77f713f35f0f3d2c9e6cf6b9c6ca423a8adc5`  
		Last Modified: Fri, 30 May 2025 17:42:17 GMT  
		Size: 15.5 MB (15527348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf28d20cc8b8f5a674d7916cd293e01a919fb383e0f57bf206082bb65a17e284`  
		Last Modified: Fri, 30 May 2025 17:42:26 GMT  
		Size: 220.5 MB (220503488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-jdk-bullseye` - unknown; unknown

```console
$ docker pull openjdk@sha256:27d6397c6d41d758d135c83ee4aaa861f1da2b951cfd729ae156396e0770b68a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.5 MB (8523307 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:195f95b12a5738fdadc436831d9b592ad288bd3ccbc606762a7d505a4e470eab`

```dockerfile
```

-	Layers:
	-	`sha256:a26551b04108fd3619dce0fcc2dae4b98e01b15c285bd3caf4fa313191896325`  
		Last Modified: Fri, 30 May 2025 17:42:17 GMT  
		Size: 8.5 MB (8504547 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1b42ae853d16935639435779807b4c2a39d9c3d656c0a92aa46e7af23c9a44a6`  
		Last Modified: Fri, 30 May 2025 17:42:16 GMT  
		Size: 18.8 KB (18760 bytes)  
		MIME: application/vnd.in-toto+json
