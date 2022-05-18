## `openjdk:19-ea-22-jdk-slim`

```console
$ docker pull openjdk@sha256:7c5db088a7d2a74ae1ce2d9c096b333c9f734e9db819a480e23e5bc7ac60cb35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; arm64 variant v8

### `openjdk:19-ea-22-jdk-slim` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:e419c9482d03d27e22d1e42299f9fe18b95395ead4e810e1d26e09a779dea202
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.2 MB (226162805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b0587b23c9f32a4addea160818cfe30a449c583d9f14a31bf7dce0015bb53db`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 11 May 2022 00:46:59 GMT
ADD file:158a0e401328bd7c0d49b9e8539186098967218f1b1a8c811f4398d29b74397f in / 
# Wed, 11 May 2022 00:47:00 GMT
CMD ["bash"]
# Wed, 11 May 2022 14:15:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 11 May 2022 14:15:57 GMT
ENV JAVA_HOME=/usr/local/openjdk-19
# Wed, 11 May 2022 14:15:58 GMT
ENV PATH=/usr/local/openjdk-19/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 11 May 2022 14:15:59 GMT
ENV LANG=C.UTF-8
# Wed, 18 May 2022 01:02:46 GMT
ENV JAVA_VERSION=19-ea+22
# Wed, 18 May 2022 01:02:59 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk19/22/GPL/openjdk-19-ea+22_linux-x64_bin.tar.gz'; 			downloadSha256='38430a128f794293c22ccaadbf7528f60a021055de72d33e210e9cf8e3a12aa6'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk19/22/GPL/openjdk-19-ea+22_linux-aarch64_bin.tar.gz'; 			downloadSha256='6884df76f084c7c190b86bac76643132226ba99ebbb61352b1050494fae20e17'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Wed, 18 May 2022 01:02:59 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:dfdd5ffb257742b891ccad9400a77dad2a6260b2451e0f5e48a9ade1d17a87ec`  
		Last Modified: Wed, 11 May 2022 00:53:46 GMT  
		Size: 30.1 MB (30065693 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb5ad7be01b68fe78dada799da391fe706a6e51b7a0ec158e40069f53de08619`  
		Last Modified: Wed, 11 May 2022 14:33:48 GMT  
		Size: 1.4 MB (1361175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a004f38db0a2b6e1af34fcf3c0255753069835785a515d3695bccb07934824ae`  
		Last Modified: Wed, 18 May 2022 01:15:47 GMT  
		Size: 194.7 MB (194735937 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
