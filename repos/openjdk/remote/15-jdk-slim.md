## `openjdk:15-jdk-slim`

```console
$ docker pull openjdk@sha256:c4949b03cc9735eb6c1dab1c8d7119429e6409cc1b9f5da4d17d08dd1b37351d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `openjdk:15-jdk-slim` - linux; amd64

```console
$ docker pull openjdk@sha256:5e6f1e52a61c48c72d628a80ee2cf6498eacb0a3b12d50a473d730f86ec6df0b
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.5 MB (226463720 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aec60dda870885b6567f4528979a412c6c26b2b9e717dafea36425bf565a50e2`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 04 Aug 2020 15:42:51 GMT
ADD file:3af3091e7d2bb40bc1e6550eb5ea290badc6bbf3339105626f245a963cc11450 in / 
# Tue, 04 Aug 2020 15:42:51 GMT
CMD ["bash"]
# Wed, 05 Aug 2020 00:41:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 05 Aug 2020 00:41:10 GMT
ENV LANG=C.UTF-8
# Wed, 05 Aug 2020 00:42:37 GMT
ENV JAVA_HOME=/usr/local/openjdk-15
# Wed, 05 Aug 2020 00:42:37 GMT
ENV PATH=/usr/local/openjdk-15/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Aug 2020 00:42:38 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Fri, 07 Aug 2020 23:31:58 GMT
ENV JAVA_VERSION=15
# Fri, 07 Aug 2020 23:32:12 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		arm64 | aarch64) 			downloadUrl=https://download.java.net/java/GA/jdk15/779bf45e88a44cbd9ea6621d33e33db1/35/GPL/openjdk-15_linux-aarch64_bin.tar.gz; 			downloadSha256=e5b7110c2fb889096b4fa5942b51c6b12dd892ca4325861d58131cad737a743b; 			;; 		amd64 | i386:x86-64) 			downloadUrl=https://download.java.net/java/GA/jdk15/779bf45e88a44cbd9ea6621d33e33db1/35/GPL/openjdk-15_linux-x64_bin.tar.gz; 			downloadSha256=38ee0f312e507b1a32b09e558552091cf249933bfc6918ae3cfa52406247885c; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O openjdk.tgz "$downloadUrl" --progress=dot:giga; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		javac --version; 	java --version
# Fri, 07 Aug 2020 23:32:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:bf59529304463f62efa7179fa1a32718a611528cc4ce9f30c0d1bbc6724ec3fb`  
		Last Modified: Tue, 04 Aug 2020 15:49:09 GMT  
		Size: 27.1 MB (27092121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:092c9b8e633fd73a2b448815d56f09aebf34c733300cd7747008b81fe7724a02`  
		Last Modified: Wed, 05 Aug 2020 00:48:13 GMT  
		Size: 3.2 MB (3248431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d928f01bcfe3ef1a57ed4d498cdf89218aa77e123cd6f78f8ec01046a6cb842`  
		Last Modified: Wed, 05 Aug 2020 00:49:13 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:408ccf41426f37831df27f54498a79d33e544ba8ca707ebf7a91ba431b8108c7`  
		Last Modified: Fri, 07 Aug 2020 23:36:58 GMT  
		Size: 196.1 MB (196122957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:15-jdk-slim` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:e8992be425bcd8543e0e5cd7de62b474537f4da25415444a0b813eeeb9e4e9b9
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **204.2 MB (204184300 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b5b6485c1538f8a1f5b2f980f560b2fd5226e8a0db2c21ecb92d39f550d9eca`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 04 Aug 2020 06:57:29 GMT
ADD file:90ba7821623ab55fc1073647cc611cc45f5e306ade734910e587021971483eec in / 
# Tue, 04 Aug 2020 06:57:31 GMT
CMD ["bash"]
# Tue, 04 Aug 2020 14:37:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 04 Aug 2020 14:37:59 GMT
ENV LANG=C.UTF-8
# Tue, 04 Aug 2020 14:39:36 GMT
ENV JAVA_HOME=/usr/local/openjdk-15
# Tue, 04 Aug 2020 14:39:38 GMT
ENV PATH=/usr/local/openjdk-15/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Aug 2020 14:39:40 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Sat, 08 Aug 2020 00:17:33 GMT
ENV JAVA_VERSION=15
# Sat, 08 Aug 2020 00:19:24 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		arm64 | aarch64) 			downloadUrl=https://download.java.net/java/GA/jdk15/779bf45e88a44cbd9ea6621d33e33db1/35/GPL/openjdk-15_linux-aarch64_bin.tar.gz; 			downloadSha256=e5b7110c2fb889096b4fa5942b51c6b12dd892ca4325861d58131cad737a743b; 			;; 		amd64 | i386:x86-64) 			downloadUrl=https://download.java.net/java/GA/jdk15/779bf45e88a44cbd9ea6621d33e33db1/35/GPL/openjdk-15_linux-x64_bin.tar.gz; 			downloadSha256=38ee0f312e507b1a32b09e558552091cf249933bfc6918ae3cfa52406247885c; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O openjdk.tgz "$downloadUrl" --progress=dot:giga; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		javac --version; 	java --version
# Sat, 08 Aug 2020 00:19:34 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3742235f1882fee5cca1effc4ca0f0c7c180bbe169800a85daedcf3968b0d8f0`  
		Last Modified: Tue, 04 Aug 2020 07:04:03 GMT  
		Size: 25.8 MB (25849301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:922e570bcbcde7895ddbc3bbb3f1a8549556b50b0dd457e10ced5a0c781b7a30`  
		Last Modified: Tue, 04 Aug 2020 14:44:30 GMT  
		Size: 3.1 MB (3101424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df4e167d9cd8db4f2afa7f1dda727540c335afc97d682961dfb9114c765163d1`  
		Last Modified: Tue, 04 Aug 2020 14:46:02 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:282dd754a583d0dd1cb0665ae3e2f85c8446ffba2dc00b6caf48121b19b62e2b`  
		Last Modified: Sat, 08 Aug 2020 00:26:46 GMT  
		Size: 175.2 MB (175233364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
