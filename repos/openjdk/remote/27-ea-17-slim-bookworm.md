## `openjdk:27-ea-17-slim-bookworm`

```console
$ docker pull openjdk@sha256:793fad8040dad5b538eb9e1e96966123a9b43c57a2dce59a08c683842a89766e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:27-ea-17-slim-bookworm` - linux; amd64

```console
$ docker pull openjdk@sha256:277b7e4ce7704e359a717383def43c02e5e20eb6d8dc425be3e0cfcb0cc52427
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.3 MB (261286646 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db60173f98b2d4d7ab253ff3635fec5024294464465685922ea33249872d0fbc`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1775433600'
# Tue, 14 Apr 2026 00:01:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 14 Apr 2026 00:01:47 GMT
ENV JAVA_HOME=/usr/local/openjdk-27
# Tue, 14 Apr 2026 00:01:47 GMT
ENV PATH=/usr/local/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Apr 2026 00:01:47 GMT
ENV LANG=C.UTF-8
# Tue, 14 Apr 2026 00:01:47 GMT
ENV JAVA_VERSION=27-ea+17
# Tue, 14 Apr 2026 00:01:47 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/17/GPL/openjdk-27-ea+17_linux-x64_bin.tar.gz'; 			downloadSha256='9052972f914c38a9c00c5d8104a0b58217438f9a672ae7abead7c12347bb0d7c'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/17/GPL/openjdk-27-ea+17_linux-aarch64_bin.tar.gz'; 			downloadSha256='c2be8295243785a5077e17817615b5f355a643367e44eef5972e58fcbd8bde4b'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 14 Apr 2026 00:01:47 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:da539b6761059a0a114c6671f1267b57445e3a54da023db5c28be019e40f0284`  
		Last Modified: Tue, 07 Apr 2026 00:11:03 GMT  
		Size: 28.2 MB (28236332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:053cc577ea6ce4f4ac4ec16c34da411dae532aefd703606386e2935011297f22`  
		Last Modified: Tue, 14 Apr 2026 00:02:07 GMT  
		Size: 4.0 MB (4030682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9457170be57daa142f62406edeb6553c3725cd9516fbbd5f41344491c5976043`  
		Last Modified: Tue, 14 Apr 2026 00:02:13 GMT  
		Size: 229.0 MB (229019632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-17-slim-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:28a35b1ad56dd7ce1a2a791c09227f619e47188831a35850a5be74e4ef2a4be4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2666678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a19c41f2dd6719f9c0efd1ffc2eb8d2cd82eeb3be39b670fb17cc30adbd75b0b`

```dockerfile
```

-	Layers:
	-	`sha256:e61c0d7260c261cfc722d1b7dbfe244a2fb74a395784750c0e48d91bb3474bd8`  
		Last Modified: Tue, 14 Apr 2026 00:02:07 GMT  
		Size: 2.6 MB (2649807 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:018eaf59dc8813fd547eae28a385e0f5ce0879e8a85bc79bafb93929112a825b`  
		Last Modified: Tue, 14 Apr 2026 00:02:06 GMT  
		Size: 16.9 KB (16871 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:27-ea-17-slim-bookworm` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:1625b1e7c8e50a7c447f53c0970c4038b9fb28ac0ea43d8f03ce17396551844b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.9 MB (258945151 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae05464a506f7962eb6d108efd5b09a2e011ca41627a4ecfe53edf5c12d56911`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1775433600'
# Tue, 14 Apr 2026 00:02:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 14 Apr 2026 00:02:42 GMT
ENV JAVA_HOME=/usr/local/openjdk-27
# Tue, 14 Apr 2026 00:02:42 GMT
ENV PATH=/usr/local/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Apr 2026 00:02:42 GMT
ENV LANG=C.UTF-8
# Tue, 14 Apr 2026 00:02:42 GMT
ENV JAVA_VERSION=27-ea+17
# Tue, 14 Apr 2026 00:02:42 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/17/GPL/openjdk-27-ea+17_linux-x64_bin.tar.gz'; 			downloadSha256='9052972f914c38a9c00c5d8104a0b58217438f9a672ae7abead7c12347bb0d7c'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/17/GPL/openjdk-27-ea+17_linux-aarch64_bin.tar.gz'; 			downloadSha256='c2be8295243785a5077e17817615b5f355a643367e44eef5972e58fcbd8bde4b'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 14 Apr 2026 00:02:42 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1dbbb2db815c2527e90ef5a3e4dfb957cfe7b61b6a7fc59722f1f64b1a1b611e`  
		Last Modified: Tue, 07 Apr 2026 00:10:39 GMT  
		Size: 28.1 MB (28116166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4383ec0569e55a1d772b7938f7ec13eebacc58f64021969d4d42bb99ee54837`  
		Last Modified: Tue, 14 Apr 2026 00:03:02 GMT  
		Size: 3.9 MB (3852262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db85d806661783aa1da5d0c98756f15ffb6efcef42340fe8b298cd949307b490`  
		Last Modified: Tue, 14 Apr 2026 00:03:07 GMT  
		Size: 227.0 MB (226976723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-17-slim-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:67d47407b53ae18523b336a2376b9144f7e3a0ded816073661f37f447151b340
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2666431 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f678bf81c8dfbd1270cc90ebf87f8a583784816fd0e4d9eaef46454877155f23`

```dockerfile
```

-	Layers:
	-	`sha256:d36e25825f7b67dd525d8cc424978d231c1c73c5ba01c0a7ada6273cf5bba112`  
		Last Modified: Tue, 14 Apr 2026 00:03:02 GMT  
		Size: 2.6 MB (2649441 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ac0721f8e497f59af0985f93c9481d748e3a400432d88e3150cc8f78161bbdbe`  
		Last Modified: Tue, 14 Apr 2026 00:03:02 GMT  
		Size: 17.0 KB (16990 bytes)  
		MIME: application/vnd.in-toto+json
