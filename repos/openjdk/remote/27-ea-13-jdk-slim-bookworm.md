## `openjdk:27-ea-13-jdk-slim-bookworm`

```console
$ docker pull openjdk@sha256:35504e5bc2e94075d2b56d8014ed1aa08bcc0cbee7d7bbc05fdc786452fbb013
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:27-ea-13-jdk-slim-bookworm` - linux; amd64

```console
$ docker pull openjdk@sha256:d268657a960db277b45b6f233bb17acd82a5d3739ee42a99d2d680898bc21ff6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **260.9 MB (260873540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9661c1e46dda6a26e1cc9fa00dbf97951d4a8fa0bbdb607eed4139ce74a1866d`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 22:46:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:46:36 GMT
ENV JAVA_HOME=/usr/local/openjdk-27
# Mon, 16 Mar 2026 22:46:36 GMT
ENV PATH=/usr/local/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 16 Mar 2026 22:46:36 GMT
ENV LANG=C.UTF-8
# Mon, 16 Mar 2026 22:46:36 GMT
ENV JAVA_VERSION=27-ea+13
# Mon, 16 Mar 2026 22:46:36 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/13/GPL/openjdk-27-ea+13_linux-x64_bin.tar.gz'; 			downloadSha256='abf2fddc7c040d0da78ea21bf8a24e8886b7db5b0451535b1382c8d04555a3a6'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/13/GPL/openjdk-27-ea+13_linux-aarch64_bin.tar.gz'; 			downloadSha256='2279406d233d34ad8cd779ec6d67043d77c66a16ba54b2b8085cc3a8e8709de7'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Mon, 16 Mar 2026 22:46:36 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:6db0909c4473287ed4d1f950d26b8bc5b7b4206d365a0e7740cb89e46979153e`  
		Last Modified: Mon, 16 Mar 2026 21:52:32 GMT  
		Size: 28.2 MB (28236225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b925171588e1f1df732aea17854571daa7d7ad0b13349255401a9b466b44342`  
		Last Modified: Mon, 16 Mar 2026 22:46:56 GMT  
		Size: 4.0 MB (4029186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faacf44d040f0b5c4040833242306e2f3ff94b339e815ac0dc1df57c2bc496e4`  
		Last Modified: Mon, 16 Mar 2026 22:47:01 GMT  
		Size: 228.6 MB (228608129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-13-jdk-slim-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:736a224cd7d119f9beb702c1ac0c2618f89b5e549d4a9d4e2d33a86ebce36b01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2666678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82323ed23ab4e2a4f958d348188be1a65a5b4dde27e48bfee492e90772c2b6b6`

```dockerfile
```

-	Layers:
	-	`sha256:c6a99756d6a9c3fde64dbdc246a6c0060e9951f5bcd55cd67c8ce9c39e4315dd`  
		Last Modified: Mon, 16 Mar 2026 22:46:56 GMT  
		Size: 2.6 MB (2649807 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:98de7e3e3c4e59cbf9554becf705b714cbe804ce3f825e55f51c9d5aa85575ec`  
		Last Modified: Mon, 16 Mar 2026 22:46:56 GMT  
		Size: 16.9 KB (16871 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:27-ea-13-jdk-slim-bookworm` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:8cecbd5d16a2d849787a6d6ceb6bb107da5c7f142b567982cbd438cfd16c6e4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.5 MB (258535562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:735d65bae8f0a8101045be19dd7c86019576bddf4a00ec45d2c9622a75799682`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 22:48:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:48:35 GMT
ENV JAVA_HOME=/usr/local/openjdk-27
# Mon, 16 Mar 2026 22:48:35 GMT
ENV PATH=/usr/local/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 16 Mar 2026 22:48:35 GMT
ENV LANG=C.UTF-8
# Mon, 16 Mar 2026 22:48:35 GMT
ENV JAVA_VERSION=27-ea+13
# Mon, 16 Mar 2026 22:48:35 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/13/GPL/openjdk-27-ea+13_linux-x64_bin.tar.gz'; 			downloadSha256='abf2fddc7c040d0da78ea21bf8a24e8886b7db5b0451535b1382c8d04555a3a6'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/13/GPL/openjdk-27-ea+13_linux-aarch64_bin.tar.gz'; 			downloadSha256='2279406d233d34ad8cd779ec6d67043d77c66a16ba54b2b8085cc3a8e8709de7'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Mon, 16 Mar 2026 22:48:35 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:d997cc310c981ac52155d0d9fe28888b261a7746a3877bb0ca848fd1a83d319a`  
		Last Modified: Mon, 16 Mar 2026 21:53:12 GMT  
		Size: 28.1 MB (28116065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f190a8074d3f2892af8f1a8713ebe6e853d0d1475d9dee14319cd3bff288413`  
		Last Modified: Mon, 16 Mar 2026 22:48:56 GMT  
		Size: 3.9 MB (3851965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd21af88c3af2b0b4a84f18e91ab9295571516060b15718ec71cd45c88f235ed`  
		Last Modified: Mon, 16 Mar 2026 22:49:01 GMT  
		Size: 226.6 MB (226567532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-13-jdk-slim-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:41b8dca56139b43b6044543342e0f236462bf58aefab5ed490206d7c38b3cc4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2666431 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:493ceeced368f2e985dd874f155bf4399f73643e6c1663dcdee3f93ecfc377f6`

```dockerfile
```

-	Layers:
	-	`sha256:96a2c0c3659e39597a028fa72048d1a1551647047ffeb078d90e9045a92a297b`  
		Last Modified: Mon, 16 Mar 2026 22:48:56 GMT  
		Size: 2.6 MB (2649441 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:04a3a8c6f6db576709f21d23c1ca22fa16a162acba76aac6d45f1844c0f5c752`  
		Last Modified: Mon, 16 Mar 2026 22:48:55 GMT  
		Size: 17.0 KB (16990 bytes)  
		MIME: application/vnd.in-toto+json
