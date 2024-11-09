## `openjdk:24-ea-23-slim-bookworm`

```console
$ docker pull openjdk@sha256:82d803e847f6974b5233693be13b7808f9e2205d27fb26834d6ca9697862ee27
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `openjdk:24-ea-23-slim-bookworm` - linux; amd64

```console
$ docker pull openjdk@sha256:9fbab85a7533a3640229f61f8bbf738b4a2e12b0fc369a8d39249ff87728c737
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.7 MB (246678656 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15023c3c9ef12bfb4f46807542bb2123fcce3d6e74414df9facd66440fad06b2`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 17 Oct 2024 00:20:29 GMT
ADD file:90b9dd8f12120e8b2cd3ece45fcbe8af67e40565e2032a40f64bd921c43e2ce7 in / 
# Thu, 17 Oct 2024 00:20:30 GMT
CMD ["bash"]
# Thu, 07 Nov 2024 19:48:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 07 Nov 2024 19:48:11 GMT
ENV JAVA_HOME=/usr/local/openjdk-24
# Thu, 07 Nov 2024 19:48:11 GMT
ENV PATH=/usr/local/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 07 Nov 2024 19:48:11 GMT
ENV LANG=C.UTF-8
# Thu, 07 Nov 2024 19:48:11 GMT
ENV JAVA_VERSION=24-ea+23
# Thu, 07 Nov 2024 19:48:11 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/23/GPL/openjdk-24-ea+23_linux-x64_bin.tar.gz'; 			downloadSha256='4a83df6c5ba87f963cb8f7830f1ddef7dbe387b6884749411cdd4db6f3be6ee4'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/23/GPL/openjdk-24-ea+23_linux-aarch64_bin.tar.gz'; 			downloadSha256='76fba0034d8bd3edd8983162ebe459dfcdeb8d19e0202eb42803716fedf61a32'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Thu, 07 Nov 2024 19:48:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:a480a496ba95a197d587aa1d9e0f545ca7dbd40495a4715342228db62b67c4ba`  
		Last Modified: Thu, 17 Oct 2024 00:23:58 GMT  
		Size: 29.1 MB (29126289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ded681902db283d40b631d7942038fc08f87eff1559a0ac7c19f129a2c30adba`  
		Last Modified: Sat, 09 Nov 2024 02:06:34 GMT  
		Size: 4.0 MB (4018041 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8a4ea45c914c999d041762d1546d06456ef0335be315f47f65f8df69c8fb465`  
		Last Modified: Sat, 09 Nov 2024 02:06:37 GMT  
		Size: 213.5 MB (213534326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-ea-23-slim-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:9953619d2d9aedf72c0dd15aca87576ee4a00e1625295f955a0b0dc8ae0677e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2535314 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce36d9bfb88b4559f517ce40146df36c2cbfa716981478e6edf3f165dcb81ed9`

```dockerfile
```

-	Layers:
	-	`sha256:f0cf96cc157b73561d057c2ab0a4198fc53570935dd0e222cefdf8a7fb07c323`  
		Last Modified: Sat, 09 Nov 2024 02:06:34 GMT  
		Size: 2.5 MB (2516068 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:495ab8e74cf2b48f1604b49f43671ed659ee8994e89962bf10ff454bd4e0f4b3`  
		Last Modified: Sat, 09 Nov 2024 02:06:34 GMT  
		Size: 19.2 KB (19246 bytes)  
		MIME: application/vnd.in-toto+json
