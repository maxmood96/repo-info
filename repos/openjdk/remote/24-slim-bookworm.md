## `openjdk:24-slim-bookworm`

```console
$ docker pull openjdk@sha256:c33d3e312a3eedb700522edf93805400835f90063ff5f7f1bfa3415acc9c0a43
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:24-slim-bookworm` - linux; amd64

```console
$ docker pull openjdk@sha256:dde654af5f9ee1c729020a737ff52b49d8268ddc2a9e502f74f01e1629ef2917
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **245.2 MB (245157427 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ccf1198fe40a70e446ef4b37399282af0a7c7ac6b04d0e8f59c0dfbddcbbbb5`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 29 Aug 2024 18:48:14 GMT
ADD file:d13afefcc2b0b02b598a3ac2598fe2187db41de1e17820e5b600a955b1429d59 in / 
# Thu, 29 Aug 2024 18:48:14 GMT
CMD ["bash"]
# Thu, 29 Aug 2024 18:48:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 29 Aug 2024 18:48:14 GMT
ENV JAVA_HOME=/usr/local/openjdk-24
# Thu, 29 Aug 2024 18:48:14 GMT
ENV PATH=/usr/local/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 29 Aug 2024 18:48:14 GMT
ENV LANG=C.UTF-8
# Thu, 29 Aug 2024 18:48:14 GMT
ENV JAVA_VERSION=24-ea+13
# Thu, 29 Aug 2024 18:48:14 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/13/GPL/openjdk-24-ea+13_linux-x64_bin.tar.gz'; 			downloadSha256='6ff78227fb6865113ff0e844c0e3dbbd3c3fee0fd03b4a3b3f7134390f785bd4'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/13/GPL/openjdk-24-ea+13_linux-aarch64_bin.tar.gz'; 			downloadSha256='21518bb62faf883eff4bfb1e2c69a5b50d6b3e96b30b0a111f1d1f41a4205fae'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Thu, 29 Aug 2024 18:48:14 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:a2318d6c47ec9cac5acc500c47c79602bcf953cec711a18bc898911a0984365b`  
		Last Modified: Wed, 04 Sep 2024 22:34:17 GMT  
		Size: 29.1 MB (29126484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39aa56e12737b45f3a3b97a7452140be71f251e15ac1ceda86d8526ddfb0537d`  
		Last Modified: Wed, 04 Sep 2024 23:11:37 GMT  
		Size: 4.0 MB (4018053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f55905c2b3831576b8f98e4d55833b36815e7a21e4390065da2c8185388a1800`  
		Last Modified: Wed, 04 Sep 2024 23:11:40 GMT  
		Size: 212.0 MB (212012890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-slim-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:24707ca74caec471f73798cfbd647270a08efb669794810eec8b84d9d80d98ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2384536 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f3585caa4674daeef62eb2cae3d80f40784b828875ecb69c25c21632eede4c9`

```dockerfile
```

-	Layers:
	-	`sha256:77ac76c0e65340b315b5d3ed66e864822731b014756b08b97f99ced932107273`  
		Last Modified: Wed, 04 Sep 2024 23:11:37 GMT  
		Size: 2.4 MB (2365306 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3f4361dcccf64cfaa8726874e7cef7a1a549c4c51e57971320cdfea481ab0107`  
		Last Modified: Wed, 04 Sep 2024 23:11:37 GMT  
		Size: 19.2 KB (19230 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:24-slim-bookworm` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:bb063b025d9239925388790df68efc690e416d07038014361100fa7aba9dd216
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.8 MB (242848298 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9564f516338f2e3213159ee6e3355bad380a095ce85d2cf7f2ac19e159dc98c3`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 29 Aug 2024 18:48:14 GMT
ADD file:06a1877f1e100122a40ed52ce771bfa7e2ab3d28323780f58f1e5b57c1e576f9 in / 
# Thu, 29 Aug 2024 18:48:14 GMT
CMD ["bash"]
# Thu, 29 Aug 2024 18:48:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 29 Aug 2024 18:48:14 GMT
ENV JAVA_HOME=/usr/local/openjdk-24
# Thu, 29 Aug 2024 18:48:14 GMT
ENV PATH=/usr/local/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 29 Aug 2024 18:48:14 GMT
ENV LANG=C.UTF-8
# Thu, 29 Aug 2024 18:48:14 GMT
ENV JAVA_VERSION=24-ea+13
# Thu, 29 Aug 2024 18:48:14 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/13/GPL/openjdk-24-ea+13_linux-x64_bin.tar.gz'; 			downloadSha256='6ff78227fb6865113ff0e844c0e3dbbd3c3fee0fd03b4a3b3f7134390f785bd4'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/13/GPL/openjdk-24-ea+13_linux-aarch64_bin.tar.gz'; 			downloadSha256='21518bb62faf883eff4bfb1e2c69a5b50d6b3e96b30b0a111f1d1f41a4205fae'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Thu, 29 Aug 2024 18:48:14 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:92c3b3500be621c72c7ac6432a9d8f731f145f4a1535361ffd3a304e55f7ccda`  
		Last Modified: Wed, 04 Sep 2024 21:42:36 GMT  
		Size: 29.2 MB (29156545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a1ad1a7b135cfc20b14fe8f939339288000b4c174fe96fc371a457db5dda174`  
		Last Modified: Thu, 05 Sep 2024 12:58:44 GMT  
		Size: 3.8 MB (3833434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0773ae8031112d4f7bcf08f66e1dcfe7be9c5a740303f97577da8735fe9712fb`  
		Last Modified: Thu, 05 Sep 2024 12:58:49 GMT  
		Size: 209.9 MB (209858319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-slim-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:6244c081eafe4a599d08e85d8567732a2b765c2fac5be770ce08749b219d0e59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2385295 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f919116de01b2f297e933915b1fc6d189bc768526e2341a8d706e73c0b4eac76`

```dockerfile
```

-	Layers:
	-	`sha256:9df175981ffefe7a4b872539e504aacc4995984884fe277eaccdf642ecfa850f`  
		Last Modified: Thu, 05 Sep 2024 12:58:44 GMT  
		Size: 2.4 MB (2365660 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3ed88ee1e9f3416af671fcf36305d799f4ac635928dc8093d9ea448d97a162cc`  
		Last Modified: Thu, 05 Sep 2024 12:58:44 GMT  
		Size: 19.6 KB (19635 bytes)  
		MIME: application/vnd.in-toto+json
