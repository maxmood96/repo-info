## `clojure:temurin-8-tools-deps-1.12.0.1530-bookworm-slim`

```console
$ docker pull clojure@sha256:35ba02c9707df14dc0551678b3f748423aef45ceefe1166b094ae8a82d766dd0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-1.12.0.1530-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:9b2254b522c3a35847b708f6162c89e428b3de0f20bc2db5777e03696c2b3a34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.5 MB (152473088 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6980950865b7654442a9f84fd99ca1edd8d27bc840057d4b8325d88e10bf667e`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 13 May 2025 03:53:36 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1747699200'
# Tue, 13 May 2025 03:53:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 May 2025 03:53:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 May 2025 03:53:36 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Tue, 13 May 2025 03:53:36 GMT
WORKDIR /tmp
# Tue, 13 May 2025 03:53:36 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 13 May 2025 03:53:36 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:61320b01ae5e0798393ef25f2dc72faf43703e60ba089b07d7170acbabbf8f62`  
		Last Modified: Tue, 03 Jun 2025 13:30:15 GMT  
		Size: 28.2 MB (28225330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:030240ce91afa5acc5a765686455f19835f5f8a6c1531cf4302b9bb15b62cba9`  
		Last Modified: Tue, 03 Jun 2025 05:15:20 GMT  
		Size: 54.7 MB (54716183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5679783b2a22299cbca9ce1045925a77dbd8d0d6b5acf5f3473216fc52699e2b`  
		Last Modified: Tue, 03 Jun 2025 05:15:21 GMT  
		Size: 69.5 MB (69530932 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d08deac548f3cf1b06982e58fa6d11d2af833ef02f13048e65e9398eb13ca8c2`  
		Last Modified: Tue, 03 Jun 2025 05:15:19 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.0.1530-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:3f149457ba1bb3c95572b00b6122665fa65519e751406e8f2307822ebf56cc8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5097399 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bba706a79ad61dba1d6b447d592094cad58d78da5224a9edec390c9ccadc5546`

```dockerfile
```

-	Layers:
	-	`sha256:784aa70bb2bca438deace330ca82d529bd72291f92fc97559479ca8349eefb54`  
		Last Modified: Tue, 03 Jun 2025 05:15:19 GMT  
		Size: 5.1 MB (5083108 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:194632867012480983eec78419a20fe40afb7c16f4556cfefca922e31574ad77`  
		Last Modified: Tue, 03 Jun 2025 05:15:19 GMT  
		Size: 14.3 KB (14291 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-1.12.0.1530-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:f41349c1c3822eb7f270b8cff4a8b6a5009674ab9d2e5f01caef24e2866795e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.3 MB (151282812 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:863bb6b0a462b608a6b340123e637e61b6c8b91d1224db436d2f7deaada24853`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 13 May 2025 03:53:36 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1747699200'
# Tue, 13 May 2025 03:53:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 May 2025 03:53:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 May 2025 03:53:36 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Tue, 13 May 2025 03:53:36 GMT
WORKDIR /tmp
# Tue, 13 May 2025 03:53:36 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 13 May 2025 03:53:36 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:b16f1b16678093d11ecfece1004207a40f9bc1b7d9d1d16a070c1db552038818`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 28.1 MB (28065280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a417e3b74fbb7215b9587254b3c223d093abcb78011dfafa76141304d521fabe`  
		Last Modified: Tue, 03 Jun 2025 10:28:14 GMT  
		Size: 53.8 MB (53830503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efdba17d3714a942ed64d1d37cdac0b0b837027f5c07ac93354ac85df75309fd`  
		Last Modified: Tue, 03 Jun 2025 10:34:54 GMT  
		Size: 69.4 MB (69386384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d000ab8caa00ee502028b028de242c175129395c963e176e91b6f7a4cff84281`  
		Last Modified: Tue, 03 Jun 2025 10:34:52 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.0.1530-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:352718e0236480fbe7576067d4dc469437f7c747f84a94d5afa5a5eda6d79f92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5103976 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98c1abcba1b2778467e78a30b2eb3b24e2ea6436bad05fc0debb494639f33481`

```dockerfile
```

-	Layers:
	-	`sha256:5c7893c4c93b75328a4ccd6942e16fb0cc4a6cba1f87e58ba827bc5ca533e894`  
		Last Modified: Tue, 03 Jun 2025 10:34:52 GMT  
		Size: 5.1 MB (5089567 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f678258dd86e2c727093e2dd5cca96b83039705fbab6c16174be5cefb761895d`  
		Last Modified: Tue, 03 Jun 2025 10:34:51 GMT  
		Size: 14.4 KB (14409 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-1.12.0.1530-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:fe7e610dae57951f9b8ba6359006109570e0133a74b793cd0fbd43cbca3af46c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.6 MB (159582695 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94b0bb26938abf70214c9fb8feb485e86b0c2e1c4e2be8706330d71f67085015`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 13 May 2025 03:53:36 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1747699200'
# Tue, 13 May 2025 03:53:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 May 2025 03:53:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 May 2025 03:53:36 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Tue, 13 May 2025 03:53:36 GMT
WORKDIR /tmp
# Tue, 13 May 2025 03:53:36 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 13 May 2025 03:53:36 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:701606535a7233566815cc9ad5f3e5853b443be5476286f6799008053dc2b03b`  
		Last Modified: Tue, 03 Jun 2025 13:39:02 GMT  
		Size: 32.1 MB (32066912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69330ccadd135120719a7f8e4da60763334e15c7b37c59d3bae3f4219bab28ff`  
		Last Modified: Tue, 03 Jun 2025 08:05:24 GMT  
		Size: 52.2 MB (52167965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb0513107d6b80075d3762454a2908d80487b98d2b90d0a812f1da37fdcbb12a`  
		Last Modified: Tue, 03 Jun 2025 08:16:31 GMT  
		Size: 75.3 MB (75347174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb9cd4ef6c7cd598133486197e5c736f5abc8f7e6e923cfe34dc1e917ac20b5f`  
		Last Modified: Tue, 03 Jun 2025 08:16:29 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.0.1530-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:aacd07d3851bdc6d50e0ad014e275e99e2db7487d3d1b3bbeeeb196a20b4eed6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5103198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a15b47bd83c4dba196510c174d5da4807de0f0e321c55284bc2a74cd31716616`

```dockerfile
```

-	Layers:
	-	`sha256:e11dde4759ad110b02c4f08c782fb11eed496e7c6d81de997729896c100f57b8`  
		Last Modified: Tue, 03 Jun 2025 08:16:29 GMT  
		Size: 5.1 MB (5088859 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e063819235e68d02b64896551b64cc9f6ce4dba923a814b37463579f574d7874`  
		Last Modified: Tue, 03 Jun 2025 08:16:29 GMT  
		Size: 14.3 KB (14339 bytes)  
		MIME: application/vnd.in-toto+json
