## `clojure:temurin-17-tools-deps-1.11.3.1456-bullseye-slim`

```console
$ docker pull clojure@sha256:38abc4a41cc251b9ba6937f4a9e1d1f9ff2ba0284ac48283967fa824ef733dc4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-tools-deps-1.11.3.1456-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:772252e07603f80f37a72a1f025fcb2ff6b55f24656062f520d3dec53f747b0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.1 MB (235142546 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:735e83317cdeb493e60e67ade515a91d2a691043684ea93bc8c15edf162d376c`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 28 May 2024 15:17:11 GMT
ADD file:49759b7a74bac875e3619e20ed5a9521101c7729f601d90976d0755d30e97499 in / 
# Tue, 28 May 2024 15:17:11 GMT
CMD ["bash"]
# Tue, 28 May 2024 15:17:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 28 May 2024 15:17:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 28 May 2024 15:17:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 May 2024 15:17:11 GMT
ENV CLOJURE_VERSION=1.11.3.1456
# Tue, 28 May 2024 15:17:11 GMT
WORKDIR /tmp
# Tue, 28 May 2024 15:17:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2f5edc801133c72a49e990816b0e245beb8b4e35a85524b4dd0b3fa03a4a5365 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 28 May 2024 15:17:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 28 May 2024 15:17:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 28 May 2024 15:17:11 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 28 May 2024 15:17:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:76956b537f14770ffd78afbe4f17016b2794c4b9b568325e8079089ea5c4e8cd`  
		Last Modified: Tue, 02 Jul 2024 01:29:27 GMT  
		Size: 31.4 MB (31422284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7569016283d02dc8ce9e9fd364d8a761e1c14edea190e83691f0c2d70f729836`  
		Last Modified: Tue, 02 Jul 2024 03:02:55 GMT  
		Size: 145.1 MB (145095109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:008aa7e41372209624b69f696b2a7d196330099dd773acec4c8ec00e9e1425f4`  
		Last Modified: Tue, 02 Jul 2024 03:02:54 GMT  
		Size: 58.6 MB (58624112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46a17d95b05d9304d2c2b6f014ddcdeb04952f97095e7cbb26c64e1fee887d95`  
		Last Modified: Tue, 02 Jul 2024 03:02:54 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c76ca5c1161453443b614eabbe526065726f5d1cade71ac1fa29c22fecf08204`  
		Last Modified: Tue, 02 Jul 2024 03:02:54 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.11.3.1456-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:eafbd769a6c4c93aea947267ca2182d67e93996564e9c3bd9cb87844386700a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4924784 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d2c47ff0a258b326ef48761a8c4028fca42faa30230dd7cc2fc6ae226a9b35e`

```dockerfile
```

-	Layers:
	-	`sha256:2fe21f912c4ee842579e1cad22f9686172b325f9da92479f15bf9bb619db524d`  
		Last Modified: Tue, 02 Jul 2024 03:02:54 GMT  
		Size: 4.9 MB (4909272 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:87d226869b3c61f96c26f072cf0f6770d95e3a77e8460071c8d17ee0ab7badb3`  
		Last Modified: Tue, 02 Jul 2024 03:02:53 GMT  
		Size: 15.5 KB (15512 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.11.3.1456-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:b30eab8a55ea39634d42a82c96b7590caeaaa5563169417480a762b261bd4107
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.5 MB (232520850 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:309abfcdef09a3e085edcf0b3ea6a3b9e418a36da58e2126a2b0053636e4b952`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 28 May 2024 15:17:11 GMT
ADD file:55edb70d595bba9782144ef15994a2ae5c40adeb65f6c3acd6570a0c148ffa96 in / 
# Tue, 28 May 2024 15:17:11 GMT
CMD ["bash"]
# Tue, 28 May 2024 15:17:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 28 May 2024 15:17:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 28 May 2024 15:17:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 May 2024 15:17:11 GMT
ENV CLOJURE_VERSION=1.11.3.1456
# Tue, 28 May 2024 15:17:11 GMT
WORKDIR /tmp
# Tue, 28 May 2024 15:17:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2f5edc801133c72a49e990816b0e245beb8b4e35a85524b4dd0b3fa03a4a5365 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 28 May 2024 15:17:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 28 May 2024 15:17:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 28 May 2024 15:17:11 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 28 May 2024 15:17:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:ca4da1869379178993d4f7abc946f75e7515789ff7e15c7ccfedfc8e2bfeaf6d`  
		Last Modified: Thu, 13 Jun 2024 00:43:54 GMT  
		Size: 30.1 MB (30086973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:596bc194b5ebca7f1da4f38caf179fa1b85f4f74030f397bee18262baf11f4f6`  
		Last Modified: Thu, 13 Jun 2024 11:37:54 GMT  
		Size: 143.9 MB (143892791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e33d82f9573f0413831ca11388904382571733e7c9fae65457a7119f718a125`  
		Last Modified: Thu, 13 Jun 2024 11:52:20 GMT  
		Size: 58.5 MB (58540037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebf14fa037470e485a71d2691ce32f06e79cc30dde8cacf24cdaf1060f77e317`  
		Last Modified: Thu, 13 Jun 2024 11:52:19 GMT  
		Size: 618.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a68a7f20a6a030b651bd830c8c63d47c6e6d20aae4ab1db9dfed8ca8328e456`  
		Last Modified: Thu, 13 Jun 2024 11:52:18 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.11.3.1456-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:2637e83ed2d95e4147f5beab70897457b90b2fba3357226d69c3e11c3f723830
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4931642 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16cb51e242bdf4b0a014e446e6b676f59f90c76518859c5e9869bd262cf1e102`

```dockerfile
```

-	Layers:
	-	`sha256:b3e73dc57145f5598f54513fa14669997d608dbc4bbc59ca7704d43871409d94`  
		Last Modified: Thu, 13 Jun 2024 11:52:19 GMT  
		Size: 4.9 MB (4915589 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:20a4895f67ce0d210df87fa690faafa34e7ad2c732b1b9d1e6bfd80f62322e58`  
		Last Modified: Thu, 13 Jun 2024 11:52:18 GMT  
		Size: 16.1 KB (16053 bytes)  
		MIME: application/vnd.in-toto+json
