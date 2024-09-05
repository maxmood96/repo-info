## `openjdk:23-slim-bullseye`

```console
$ docker pull openjdk@sha256:11c08b0d8b48597143ccac723dd3f033ebc0c2c0be12d175a78bbb4801eb20e5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:23-slim-bullseye` - linux; amd64

```console
$ docker pull openjdk@sha256:1a40b2b9e33c11793c43172b57f3d6c46a423166eb5d46ae164947109e7c27de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.5 MB (244451029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e73fa4882533318f911c01ccbbde31197aebd7eb627598db7ae481a87c6b4db`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 21 Aug 2024 18:48:11 GMT
ADD file:1b8ac8ec2b2cbdfc9682f076e7e579579d6df6235ed23b2e63f8eec671c52e92 in / 
# Wed, 21 Aug 2024 18:48:11 GMT
CMD ["bash"]
# Wed, 21 Aug 2024 18:48:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 21 Aug 2024 18:48:11 GMT
ENV JAVA_HOME=/usr/local/openjdk-23
# Wed, 21 Aug 2024 18:48:11 GMT
ENV PATH=/usr/local/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 21 Aug 2024 18:48:11 GMT
ENV LANG=C.UTF-8
# Wed, 21 Aug 2024 18:48:11 GMT
ENV JAVA_VERSION=23
# Wed, 21 Aug 2024 18:48:11 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/GA/jdk23/3c5b90190c68498b986a97f276efd28a/37/GPL/openjdk-23_linux-x64_bin.tar.gz'; 			downloadSha256='08fea92724127c6fa0f2e5ea0b07ff4951ccb1e2f22db3c21eebbd7347152a67'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/GA/jdk23/3c5b90190c68498b986a97f276efd28a/37/GPL/openjdk-23_linux-aarch64_bin.tar.gz'; 			downloadSha256='076dcf7078cdf941951587bf92733abacf489a6570f1df97ee35945ffebec5b7'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Wed, 21 Aug 2024 18:48:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:6533c3eba3f3cd4c840877f9245b26929fc8c22a39f42c872aa314c32c6d654b`  
		Last Modified: Wed, 04 Sep 2024 22:34:54 GMT  
		Size: 31.4 MB (31428677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efcf7c2783384c32386653507d9eadc548290a30d33c7626d32c5ebeeb08b5b2`  
		Last Modified: Wed, 04 Sep 2024 23:11:47 GMT  
		Size: 1.6 MB (1581829 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0431457d7c379e0ca5044799991cc7e7ca0bd4befec0cba4529989f07595d65`  
		Last Modified: Wed, 04 Sep 2024 23:11:53 GMT  
		Size: 211.4 MB (211440523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-slim-bullseye` - unknown; unknown

```console
$ docker pull openjdk@sha256:6d853c08cbd5a633f23435428e1f6ff50e446ef54c7b435b33b674db69c8b025
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2675244 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9a64eb4b50df2b885c10137ee50c3bc4a04639e66410f7fcdf5f53e88c1da78`

```dockerfile
```

-	Layers:
	-	`sha256:cebec851dca5d8e4dabb7ad8110fd8846b59157cf57ced9a013a7317a5a70dcc`  
		Last Modified: Wed, 04 Sep 2024 23:11:47 GMT  
		Size: 2.7 MB (2658490 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f5a1b920fd8fa579322495b685c170ed4923241848ca66392bef966b3ae32e99`  
		Last Modified: Wed, 04 Sep 2024 23:11:46 GMT  
		Size: 16.8 KB (16754 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:23-slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:0655b3971568062c6d46ab9eca7563b8cade230b8d52bc14f9843372bf115b28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.0 MB (240971675 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97ff01c2a3677f70860ac3983b7076223dd922707aa46e6d8c7ae0655d21195f`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 21 Aug 2024 18:48:11 GMT
ADD file:0802ca323252c154049da951c7da8572fb921f823341726dd7664f05c009e50c in / 
# Wed, 21 Aug 2024 18:48:11 GMT
CMD ["bash"]
# Wed, 21 Aug 2024 18:48:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 21 Aug 2024 18:48:11 GMT
ENV JAVA_HOME=/usr/local/openjdk-23
# Wed, 21 Aug 2024 18:48:11 GMT
ENV PATH=/usr/local/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 21 Aug 2024 18:48:11 GMT
ENV LANG=C.UTF-8
# Wed, 21 Aug 2024 18:48:11 GMT
ENV JAVA_VERSION=23
# Wed, 21 Aug 2024 18:48:11 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/GA/jdk23/3c5b90190c68498b986a97f276efd28a/37/GPL/openjdk-23_linux-x64_bin.tar.gz'; 			downloadSha256='08fea92724127c6fa0f2e5ea0b07ff4951ccb1e2f22db3c21eebbd7347152a67'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/GA/jdk23/3c5b90190c68498b986a97f276efd28a/37/GPL/openjdk-23_linux-aarch64_bin.tar.gz'; 			downloadSha256='076dcf7078cdf941951587bf92733abacf489a6570f1df97ee35945ffebec5b7'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Wed, 21 Aug 2024 18:48:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:172514850d5c3a8b3bc66fd0f1f345729d1b0b249cc3f053febcb64a066835da`  
		Last Modified: Wed, 04 Sep 2024 21:43:10 GMT  
		Size: 30.1 MB (30074365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95a37837d4837e78859d09e01c51430b6b2685cea6e27d41e4af3c075e3df4d5`  
		Last Modified: Thu, 05 Sep 2024 13:00:47 GMT  
		Size: 1.6 MB (1565927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a924024bf5ed4a78fece77df15fee949886d774e38720e6e4f95bd8ea8f64b3`  
		Last Modified: Thu, 05 Sep 2024 13:04:41 GMT  
		Size: 209.3 MB (209331383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-slim-bullseye` - unknown; unknown

```console
$ docker pull openjdk@sha256:acb048ae5f7d365c4be32e4897c5b9631c880bd9a8c95f904cb5b082513fc670
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2675804 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:571349018bf7ea6e02b79288c0641d7a56fd8e2f229f1c87ca2980a432346b80`

```dockerfile
```

-	Layers:
	-	`sha256:e95282469447b4544d2dc5ce0818b617f308c9641d5889a1969ae7a35fe4f2f2`  
		Last Modified: Thu, 05 Sep 2024 13:04:35 GMT  
		Size: 2.7 MB (2658742 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a3349d67153c0d236fe18ce00ee32a271657a4d8b341e59a3b64246e07fd5aaa`  
		Last Modified: Thu, 05 Sep 2024 13:04:34 GMT  
		Size: 17.1 KB (17062 bytes)  
		MIME: application/vnd.in-toto+json
