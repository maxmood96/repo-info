## `clojure:openjdk-18-tools-deps-1.10.3.1075`

```console
$ docker pull clojure@sha256:5da3b400f7d645fdb421bbe561f93ed22290a9dc15c8255f23d9393ff596db2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:openjdk-18-tools-deps-1.10.3.1075` - linux; amd64

```console
$ docker pull clojure@sha256:9c740e7854534c2c56c3ba927e8706373a9f4839ae468bb9b49fc71ba373375d
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **282.0 MB (282012373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9aff0c433d302040f65cc42acc0d6902d63f993c3d646685ff03de49cd65f0da`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 26 Jan 2022 01:40:35 GMT
ADD file:90495c24c897ec47982e200f732f8be3109fcd791691ddffae0756898f91024f in / 
# Wed, 26 Jan 2022 01:40:36 GMT
CMD ["bash"]
# Wed, 26 Jan 2022 09:18:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 26 Jan 2022 09:20:29 GMT
ENV JAVA_HOME=/usr/local/openjdk-18
# Wed, 26 Jan 2022 09:20:29 GMT
ENV PATH=/usr/local/openjdk-18/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Jan 2022 09:20:29 GMT
ENV LANG=C.UTF-8
# Tue, 08 Feb 2022 03:45:51 GMT
ENV JAVA_VERSION=18-ea+34
# Tue, 08 Feb 2022 03:46:06 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk18/34/GPL/openjdk-18-ea+34_linux-x64_bin.tar.gz'; 			downloadSha256='6811138655a3ede61c4e551db2fcc572bbf2bdfb6752777fcbf5d5b2a0affa6b'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk18/34/GPL/openjdk-18-ea+34_linux-aarch64_bin.tar.gz'; 			downloadSha256='0c60dee24ba0c181adce97eb72e4517212fe0a113ae048cb4f581e7326012812'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Tue, 08 Feb 2022 03:46:07 GMT
CMD ["jshell"]
# Tue, 08 Feb 2022 06:12:07 GMT
ENV CLOJURE_VERSION=1.10.3.1075
# Tue, 08 Feb 2022 06:12:07 GMT
WORKDIR /tmp
# Tue, 08 Feb 2022 06:12:25 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "4a6b72c9b23d348a0636813c5f59db5dda622e3b8dbb86124cbb51e3aced714d *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Tue, 08 Feb 2022 06:12:26 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Tue, 08 Feb 2022 06:12:26 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Tue, 08 Feb 2022 06:12:26 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 08 Feb 2022 06:12:26 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:5eb5b503b37671af16371272f9c5313a3e82f1d0756e14506704489ad9900803`  
		Last Modified: Wed, 26 Jan 2022 01:46:39 GMT  
		Size: 31.4 MB (31366257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc79ff7de66b9ef44dc6cd4f500aa92bd1f0b09ccd13eb0ee6441084fbb719cf`  
		Last Modified: Wed, 26 Jan 2022 09:41:32 GMT  
		Size: 1.6 MB (1582049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a91b8877fa6956069d8fc9b8695ff61c45112cf8db300a45a823ee2ef3981f3f`  
		Last Modified: Tue, 08 Feb 2022 03:59:57 GMT  
		Size: 189.0 MB (189031536 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6d0799e80b3cb5e9487b11e45a08e98631579109db4d814135bb60a7e577fcc`  
		Last Modified: Tue, 08 Feb 2022 06:20:38 GMT  
		Size: 60.0 MB (60031496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:251e214f2f4e99ce5933e497176059a67e6f513642865bacd9cb8223b2791591`  
		Last Modified: Tue, 08 Feb 2022 06:20:30 GMT  
		Size: 627.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3045c23bac159d7cccab283704166af80e95477b7af372f5dbf948402f78fe20`  
		Last Modified: Tue, 08 Feb 2022 06:20:30 GMT  
		Size: 408.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:openjdk-18-tools-deps-1.10.3.1075` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:c62e8f82b18f66674297f9b5e864e643265a0c3ea346371e0195b6bb7b325657
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **279.3 MB (279328982 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1314d56dc9f2829e7b9d34e249dfd07b56d510f298a8a9ff17c0da60157ddaeb`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 26 Jan 2022 01:42:31 GMT
ADD file:0ec6f47a8857bf8e6cef71ed8f864be7ce1790ff6ed04fd4201e7dbde4728d3a in / 
# Wed, 26 Jan 2022 01:42:31 GMT
CMD ["bash"]
# Wed, 26 Jan 2022 05:49:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 26 Jan 2022 05:52:13 GMT
ENV JAVA_HOME=/usr/local/openjdk-18
# Wed, 26 Jan 2022 05:52:14 GMT
ENV PATH=/usr/local/openjdk-18/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Jan 2022 05:52:15 GMT
ENV LANG=C.UTF-8
# Tue, 08 Feb 2022 06:27:12 GMT
ENV JAVA_VERSION=18-ea+34
# Tue, 08 Feb 2022 06:27:27 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk18/34/GPL/openjdk-18-ea+34_linux-x64_bin.tar.gz'; 			downloadSha256='6811138655a3ede61c4e551db2fcc572bbf2bdfb6752777fcbf5d5b2a0affa6b'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk18/34/GPL/openjdk-18-ea+34_linux-aarch64_bin.tar.gz'; 			downloadSha256='0c60dee24ba0c181adce97eb72e4517212fe0a113ae048cb4f581e7326012812'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Tue, 08 Feb 2022 06:27:27 GMT
CMD ["jshell"]
# Tue, 08 Feb 2022 09:32:09 GMT
ENV CLOJURE_VERSION=1.10.3.1075
# Tue, 08 Feb 2022 09:32:10 GMT
WORKDIR /tmp
# Tue, 08 Feb 2022 09:32:26 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "4a6b72c9b23d348a0636813c5f59db5dda622e3b8dbb86124cbb51e3aced714d *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Tue, 08 Feb 2022 09:32:27 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Tue, 08 Feb 2022 09:32:28 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Tue, 08 Feb 2022 09:32:28 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 08 Feb 2022 09:32:29 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:8998bd30e6a1204d13403045766edbe14f941b52087465f5d140ab63c8b113bf`  
		Last Modified: Wed, 26 Jan 2022 01:49:04 GMT  
		Size: 30.1 MB (30056774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4abf67e3e34eccefabf68f15c7d753f1a4c8e241beb1818f97e276186d54124e`  
		Last Modified: Wed, 26 Jan 2022 06:13:02 GMT  
		Size: 1.6 MB (1565889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d30ad345fa4797843c974b323f23703434d9a83c124d5556c02e70a91e6f26bb`  
		Last Modified: Tue, 08 Feb 2022 08:26:49 GMT  
		Size: 187.8 MB (187750552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67edc182f78130cdc9f6a95bb424d85a5a5483f03597fa659a80487ad05d73a5`  
		Last Modified: Tue, 08 Feb 2022 09:42:21 GMT  
		Size: 60.0 MB (59954740 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdcdf9fb6bb7fd81c5f416eb77251122fe835565b17f6f0ec5cb684d9f0f47f3`  
		Last Modified: Tue, 08 Feb 2022 09:42:13 GMT  
		Size: 622.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b818c222900176edbcfe0202b4b221beef1ddaf3c7f5f3f559223c7f9890201`  
		Last Modified: Tue, 08 Feb 2022 09:42:13 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
