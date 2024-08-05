## `openjdk:24-jdk-slim`

```console
$ docker pull openjdk@sha256:4c9d463f495cf804f76ebd6f4f22ce0e42d9d742ed6754febe6cb8e4f37912d9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:24-jdk-slim` - linux; amd64

```console
$ docker pull openjdk@sha256:57ec5377737d6b3354c8d0b0a841a91505f44702753ac3c8fe1af22e2753c924
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **245.0 MB (245035050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0520bdd6900c557db3ee813dd366862d137aa322559ba670010c408f66dd51e`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 23 Jul 2024 05:24:15 GMT
ADD file:6c4730e7b12278bc7eb83b3b9d659437c92c42fc7ee70922ae8c4bebfb56a602 in / 
# Tue, 23 Jul 2024 05:24:16 GMT
CMD ["bash"]
# Fri, 02 Aug 2024 18:51:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 02 Aug 2024 18:51:57 GMT
ENV JAVA_HOME=/usr/local/openjdk-24
# Fri, 02 Aug 2024 18:51:57 GMT
ENV PATH=/usr/local/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Aug 2024 18:51:57 GMT
ENV LANG=C.UTF-8
# Fri, 02 Aug 2024 18:51:57 GMT
ENV JAVA_VERSION=24-ea+9
# Fri, 02 Aug 2024 18:51:57 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/9/GPL/openjdk-24-ea+9_linux-x64_bin.tar.gz'; 			downloadSha256='5dd8d67a4e4059d22eb6fe7c636bf7610832380061f522aec631b69fdbaba6ae'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/9/GPL/openjdk-24-ea+9_linux-aarch64_bin.tar.gz'; 			downloadSha256='ef04b828af0fa6aca544841b01f5efda63143b81f52f1f69b2b5cf46953713a7'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 02 Aug 2024 18:51:57 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:efc2b5ad9eec05befa54239d53feeae3569ccbef689aa5e5dbfc25da6c4df559`  
		Last Modified: Tue, 23 Jul 2024 05:27:55 GMT  
		Size: 29.1 MB (29126287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70f9b2a498ed0c325a24b60a5af780c6cb65cd8fead47d6f89338be88fd0dd86`  
		Last Modified: Mon, 05 Aug 2024 18:57:46 GMT  
		Size: 4.0 MB (4016744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30824695a92fb99ad0d3d75b59f8769403a646a3297dfac9ba6c481b4a8e4da2`  
		Last Modified: Mon, 05 Aug 2024 18:57:49 GMT  
		Size: 211.9 MB (211892019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-jdk-slim` - unknown; unknown

```console
$ docker pull openjdk@sha256:383682dd7c1715fa0a1ca2c6eb75373f10f965d76186f46b8c7cdc87c2720e29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2384507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bae440edff6c49d17190a633f00fcdc8aba5b3441d4b809a4841748de9fed4c`

```dockerfile
```

-	Layers:
	-	`sha256:fff3f9330d5424b8eb0ce051b40ea13fe3d7993eb075c67f5f6f4d632fd464b2`  
		Last Modified: Mon, 05 Aug 2024 18:57:46 GMT  
		Size: 2.4 MB (2365294 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8b9f376d00a646e693bdf717d2b7d2b33215ce16e919a70b4028d0ddc843a903`  
		Last Modified: Mon, 05 Aug 2024 18:57:46 GMT  
		Size: 19.2 KB (19213 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:24-jdk-slim` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:36459d1f0257dcf48bd92b18c8981a4bad5a44dca0c7f36603702cce0321f89d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.8 MB (242753840 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bf3dc651d1a2bad42ea2e6244fcde80fca22496620b055fa3a97d9ac3a3c132`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 23 Jul 2024 04:17:51 GMT
ADD file:9b9556e1f3168a82eb85577dc07d85b2e7c1a72c5c35a4003f00042dd27b4fa2 in / 
# Tue, 23 Jul 2024 04:17:52 GMT
CMD ["bash"]
# Fri, 02 Aug 2024 18:51:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 02 Aug 2024 18:51:57 GMT
ENV JAVA_HOME=/usr/local/openjdk-24
# Fri, 02 Aug 2024 18:51:57 GMT
ENV PATH=/usr/local/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Aug 2024 18:51:57 GMT
ENV LANG=C.UTF-8
# Fri, 02 Aug 2024 18:51:57 GMT
ENV JAVA_VERSION=24-ea+9
# Fri, 02 Aug 2024 18:51:57 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/9/GPL/openjdk-24-ea+9_linux-x64_bin.tar.gz'; 			downloadSha256='5dd8d67a4e4059d22eb6fe7c636bf7610832380061f522aec631b69fdbaba6ae'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/9/GPL/openjdk-24-ea+9_linux-aarch64_bin.tar.gz'; 			downloadSha256='ef04b828af0fa6aca544841b01f5efda63143b81f52f1f69b2b5cf46953713a7'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 02 Aug 2024 18:51:57 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:262a5f25eec7a7daccd94a64695e41acca5262f481c3630ef31289616897aa40`  
		Last Modified: Tue, 23 Jul 2024 04:20:29 GMT  
		Size: 29.2 MB (29156571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c349375e2e294f7eff4dd86f726854408dbf40098a96b9250ed96a5be15a73f5`  
		Last Modified: Mon, 29 Jul 2024 16:59:58 GMT  
		Size: 3.8 MB (3829955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:691c2897de1dff47df68e3f326be6ba0c02c20af819cc0f4d69ed473f2fafb9e`  
		Last Modified: Mon, 05 Aug 2024 19:09:14 GMT  
		Size: 209.8 MB (209767314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-jdk-slim` - unknown; unknown

```console
$ docker pull openjdk@sha256:4fbb0f177282d7d402d159ba3595a40fd6aa2a0d3476f8115befab194f18a0b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2385266 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad321a40303b59988aa393168603cc7c6944cb321f4d64ab690896165c04c484`

```dockerfile
```

-	Layers:
	-	`sha256:86bd341bea229ac68d47fa83e89a7736cefd73e0bcb96002d7e7eb45c3c0e616`  
		Last Modified: Mon, 05 Aug 2024 19:09:10 GMT  
		Size: 2.4 MB (2365648 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:827b4d4f7354f763c0a58292154a8e27828a1ba52d5c3d3b2fa504d095bfcf23`  
		Last Modified: Mon, 05 Aug 2024 19:09:10 GMT  
		Size: 19.6 KB (19618 bytes)  
		MIME: application/vnd.in-toto+json
