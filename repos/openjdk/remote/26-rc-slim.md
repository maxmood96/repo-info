## `openjdk:26-rc-slim`

```console
$ docker pull openjdk@sha256:0c6b788040be481c14299cdd38ff667bc1c66b67039320e77351731f62a1af11
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:26-rc-slim` - linux; amd64

```console
$ docker pull openjdk@sha256:fad55ce45aee07cb81c588ab129ba255446f899bd18ee72d84410c57b7e7166b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **260.3 MB (260255977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d428cc2ca7f1b0b094cfc9efe74ce9215594d6a24a8385627f4b9782c977e38b`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 22:46:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:46:20 GMT
ENV JAVA_HOME=/usr/local/openjdk-26
# Mon, 16 Mar 2026 22:46:20 GMT
ENV PATH=/usr/local/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 16 Mar 2026 22:46:20 GMT
ENV LANG=C.UTF-8
# Mon, 16 Mar 2026 22:46:20 GMT
ENV JAVA_VERSION=26
# Mon, 16 Mar 2026 22:46:20 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/GA/jdk26/c3cc523845074aa0af4f5e1e1ed4151d/35/GPL/openjdk-26_linux-x64_bin.tar.gz'; 			downloadSha256='83c78367f8c81257beef72aca4bbbf8e6dac8ca2b3a4546a85879a09e6e4e128'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/GA/jdk26/c3cc523845074aa0af4f5e1e1ed4151d/35/GPL/openjdk-26_linux-aarch64_bin.tar.gz'; 			downloadSha256='403ccf451e88d0be9e1dec129fcb9318de9752121e0eb92dfa9a8cf06f249007'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Mon, 16 Mar 2026 22:46:20 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:ec781dee3f4719c2ca0dd9e73cb1d4ed834ed1a406495eb6e44b6dfaad5d1f8f`  
		Last Modified: Mon, 16 Mar 2026 21:53:19 GMT  
		Size: 29.8 MB (29775500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5e986ff02f493b590a4e04fd49df3c15187dc2c3dd2caf925936b9fdea4c5d7`  
		Last Modified: Mon, 16 Mar 2026 22:46:38 GMT  
		Size: 2.4 MB (2371124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cc1649739add7c8a5cf46c595e6b488f62bcf6d635820ecb8f53a87a87b9b1f`  
		Last Modified: Mon, 16 Mar 2026 22:46:43 GMT  
		Size: 228.1 MB (228109353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-rc-slim` - unknown; unknown

```console
$ docker pull openjdk@sha256:93ebfb97f24b1faa745463d2d1446fa620448cd328f83e38d17733c57daf7bf6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2295077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f34b4bd2ce2a6a8161eea18a6324bce72559b7caeb9db973af2d5a631f1c6235`

```dockerfile
```

-	Layers:
	-	`sha256:c7c3627b6a455cdc415e8905580b59ae5a21d13186dffac38ac1bf9dbb8a50b6`  
		Last Modified: Mon, 16 Mar 2026 22:46:38 GMT  
		Size: 2.3 MB (2278204 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b8dbecd15aba0c5ffd917b4f2406dedb1c35bbf7cbc06210202cd4cbcbc02b66`  
		Last Modified: Mon, 16 Mar 2026 22:46:38 GMT  
		Size: 16.9 KB (16873 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:26-rc-slim` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:c8d0541a05b4963e3862a486f1ebb09d6fdedf51246c905c146a3c74fc2c52f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.5 MB (258488351 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c38763c9cafbe550cdc113083b4ac76be150e72c55a165486549f164c2cb6ef0`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 22:48:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:48:24 GMT
ENV JAVA_HOME=/usr/local/openjdk-26
# Mon, 16 Mar 2026 22:48:24 GMT
ENV PATH=/usr/local/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 16 Mar 2026 22:48:24 GMT
ENV LANG=C.UTF-8
# Mon, 16 Mar 2026 22:48:24 GMT
ENV JAVA_VERSION=26
# Mon, 16 Mar 2026 22:48:24 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/GA/jdk26/c3cc523845074aa0af4f5e1e1ed4151d/35/GPL/openjdk-26_linux-x64_bin.tar.gz'; 			downloadSha256='83c78367f8c81257beef72aca4bbbf8e6dac8ca2b3a4546a85879a09e6e4e128'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/GA/jdk26/c3cc523845074aa0af4f5e1e1ed4151d/35/GPL/openjdk-26_linux-aarch64_bin.tar.gz'; 			downloadSha256='403ccf451e88d0be9e1dec129fcb9318de9752121e0eb92dfa9a8cf06f249007'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Mon, 16 Mar 2026 22:48:24 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f4badedbec24858ef2dc51256f6418328e305e9c3c5a5e093581f83425618bd5`  
		Last Modified: Mon, 16 Mar 2026 21:53:04 GMT  
		Size: 30.1 MB (30138416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dcf7337b69350895af4e223d06c5d7ff9f17a3a212ea065c033ff184f35a046`  
		Last Modified: Mon, 16 Mar 2026 22:48:45 GMT  
		Size: 2.3 MB (2314384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15d896556deb40ceff54befca19d8ec1e13cd5d2fd91b5213a29f49568832e77`  
		Last Modified: Mon, 16 Mar 2026 22:48:49 GMT  
		Size: 226.0 MB (226035551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-rc-slim` - unknown; unknown

```console
$ docker pull openjdk@sha256:acea531b447c4fabb8b739161a8fa2281c0d012807d0df9021472330bb75accc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2294834 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bbffcfb0ed6192dc579b334f3cc19c8c1135490f7c520f2c71406a1cc0c5e1f`

```dockerfile
```

-	Layers:
	-	`sha256:504d3f52178fd376e0cc80075060a97ffa88a0b18ae228efbe39063f85b84214`  
		Last Modified: Mon, 16 Mar 2026 22:48:44 GMT  
		Size: 2.3 MB (2277842 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c1546e162df6e8f99e35e1434a78fd0d2ed44463a349bcd10d063a90e727e2c4`  
		Last Modified: Mon, 16 Mar 2026 22:48:44 GMT  
		Size: 17.0 KB (16992 bytes)  
		MIME: application/vnd.in-toto+json
