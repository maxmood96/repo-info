## `openjdk:24-jdk-slim-bullseye`

```console
$ docker pull openjdk@sha256:88750379e9672ea071999c0bce80077ff64c47bb5729a0cc8988674303c078b2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:24-jdk-slim-bullseye` - linux; amd64

```console
$ docker pull openjdk@sha256:53114089661bdbfb40bb22938d1f4d5b6a69ae5ab95482643299bade63a75444
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **245.4 MB (245397327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca2ff253cd1f8598eed9e3762260a565f99a7cff86defb5504567bb74a5de8d9`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 27 Sep 2024 04:29:55 GMT
ADD file:270cda9833ffe6dfbe916662a9204a205f41c1fd440b66ec822ac00de86a5f5e in / 
# Fri, 27 Sep 2024 04:29:55 GMT
CMD ["bash"]
# Fri, 04 Oct 2024 18:48:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 04 Oct 2024 18:48:13 GMT
ENV JAVA_HOME=/usr/local/openjdk-24
# Fri, 04 Oct 2024 18:48:13 GMT
ENV PATH=/usr/local/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 04 Oct 2024 18:48:13 GMT
ENV LANG=C.UTF-8
# Fri, 04 Oct 2024 18:48:13 GMT
ENV JAVA_VERSION=24-ea+18
# Fri, 04 Oct 2024 18:48:13 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/18/GPL/openjdk-24-ea+18_linux-x64_bin.tar.gz'; 			downloadSha256='04f26aabbc1c5cf21303b08acbd073e87b08bc8522a9f23db6995356cff4c9c1'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/18/GPL/openjdk-24-ea+18_linux-aarch64_bin.tar.gz'; 			downloadSha256='8cf1e6199534b6b9c57616ec38aac5ff15846eed5e82573ecf27535848d9e810'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 04 Oct 2024 18:48:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:fa0650a893c25858ebb09921bc9b7824594e23405374a6adbcd3b4e27e28e3cf`  
		Last Modified: Fri, 27 Sep 2024 04:33:50 GMT  
		Size: 31.4 MB (31428599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6195c50a32ec5f97171d23f84f54449d284000704d84bae8f2ec9153d8dbd1b0`  
		Last Modified: Tue, 08 Oct 2024 00:01:06 GMT  
		Size: 1.6 MB (1581829 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b30612c5a8141be46365902a7a2a34e848a5b953594c0bd26039f395098375d`  
		Last Modified: Tue, 08 Oct 2024 00:01:13 GMT  
		Size: 212.4 MB (212386899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-jdk-slim-bullseye` - unknown; unknown

```console
$ docker pull openjdk@sha256:b37a3b88a1f941213525f4a10aa159a9cee3dfc0be347f82287f172913c3801d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2815122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac900c460858f46b3ed21488a1f08b8ad2984077b35b3c2f399560b38b3f067d`

```dockerfile
```

-	Layers:
	-	`sha256:adf7a57efd243e1e7bb9d3b4bf0408c8a8cad3f05cdc1db61883489ae91becde`  
		Last Modified: Tue, 08 Oct 2024 00:01:05 GMT  
		Size: 2.8 MB (2797759 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d66e719b61d29bb0bc425cfb6c34f2d6281ffc708ed5cdf0e2d949b599a5ddd8`  
		Last Modified: Tue, 08 Oct 2024 00:01:06 GMT  
		Size: 17.4 KB (17363 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:24-jdk-slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:f178ae48132eb7c90b44c6965077b11f3bc70df6645010f7d289add16191b434
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.8 MB (241849247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:394451b96d2c2544b846b56d39afcae2373232813e9f44607d90ca20d0a4a135`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 27 Sep 2024 04:38:32 GMT
ADD file:a981209c874e612fdb9f74c3315954986cfdc61cf22ab48477f2e96b3e7aeedf in / 
# Fri, 27 Sep 2024 04:38:32 GMT
CMD ["bash"]
# Fri, 04 Oct 2024 18:48:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 04 Oct 2024 18:48:13 GMT
ENV JAVA_HOME=/usr/local/openjdk-24
# Fri, 04 Oct 2024 18:48:13 GMT
ENV PATH=/usr/local/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 04 Oct 2024 18:48:13 GMT
ENV LANG=C.UTF-8
# Fri, 04 Oct 2024 18:48:13 GMT
ENV JAVA_VERSION=24-ea+18
# Fri, 04 Oct 2024 18:48:13 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/18/GPL/openjdk-24-ea+18_linux-x64_bin.tar.gz'; 			downloadSha256='04f26aabbc1c5cf21303b08acbd073e87b08bc8522a9f23db6995356cff4c9c1'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/18/GPL/openjdk-24-ea+18_linux-aarch64_bin.tar.gz'; 			downloadSha256='8cf1e6199534b6b9c57616ec38aac5ff15846eed5e82573ecf27535848d9e810'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 04 Oct 2024 18:48:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2245c7c084558dcf55e2bad9579c63dfdbd831cdbed2e063a1c25322cb793bed`  
		Last Modified: Fri, 27 Sep 2024 04:41:27 GMT  
		Size: 30.1 MB (30075158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5b5db75b1195f4426dc5c6df9f22a2bc7d6a6060252b15ba32d0b019f86936b`  
		Last Modified: Tue, 08 Oct 2024 02:35:48 GMT  
		Size: 1.6 MB (1565926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b05204ece8bbf9af7d2a88c53ebb10199c8a0a987f60a15daa4dcf936c5d24d9`  
		Last Modified: Tue, 08 Oct 2024 02:35:52 GMT  
		Size: 210.2 MB (210208163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-jdk-slim-bullseye` - unknown; unknown

```console
$ docker pull openjdk@sha256:bc4cdb58fc1e80fa069adc009af7d7ab8624c305c1aac37f333177cd50ca9207
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2814286 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41b6eb30bf84012584882da8552af352f8609fa673f3d18e3da09ec5f884e7a2`

```dockerfile
```

-	Layers:
	-	`sha256:5d6041ef7fc581324c766173218092b4d82cfce9c4699086068ec9a29f6860ae`  
		Last Modified: Tue, 08 Oct 2024 02:35:48 GMT  
		Size: 2.8 MB (2796786 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bb5f44b6b9bedca84f7db11edd633e7d25176fdd13c0c2ccad6713b4ae117b6e`  
		Last Modified: Tue, 08 Oct 2024 02:35:47 GMT  
		Size: 17.5 KB (17500 bytes)  
		MIME: application/vnd.in-toto+json
