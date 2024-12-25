## `clojure:temurin-8-tools-deps-bookworm`

```console
$ docker pull clojure@sha256:23f6fad1df0a7b1af309f13c11cff892decdb7fd60135dbd7d92cbb4681f6919
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:6494cb06446e1556952b92a95886c2cf076e4f4c9161c8502c0a88c3c875ec26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.9 MB (232875853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fe612dd38b3ecada246d8957cbe3ae2f7fa2921c30ff7f64e11c6b52e9f0986`
-	Default Command: `["clj"]`

```dockerfile
# Thu, 03 Oct 2024 17:49:34 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1734912000'
# Thu, 03 Oct 2024 17:49:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 03 Oct 2024 17:49:34 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Oct 2024 17:49:34 GMT
ENV CLOJURE_VERSION=1.12.0.1479
# Thu, 03 Oct 2024 17:49:34 GMT
WORKDIR /tmp
# Thu, 03 Oct 2024 17:49:34 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "94f29b9b66183bd58307c46fb561fd9e9148666bac13a4518a9931b6f989d830 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:0a96bdb8280554b560ffee0f2e5f9843dc7b625f28192021ee103ecbcc2d629b`  
		Last Modified: Tue, 24 Dec 2024 21:32:13 GMT  
		Size: 48.5 MB (48497066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b5728d0cc91270c67f82bfbc5eb18d02f37da7403c8da347604aeef04b1b9a2`  
		Last Modified: Tue, 24 Dec 2024 22:37:09 GMT  
		Size: 103.6 MB (103633884 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76ec0e501bf70fc5ea84829b6f34ca3250379f8a58665f4d9e4ea370a4bc093b`  
		Last Modified: Tue, 24 Dec 2024 22:37:08 GMT  
		Size: 80.7 MB (80744260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6326091088a83804c87648f87581ff95d7b9ae377074199becbb22cea9bcfb9b`  
		Last Modified: Tue, 24 Dec 2024 22:37:06 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:636711818699852f4af46ad75e337531ed4c5e7da67eb2e721d4d1073c9ba165
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7307478 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45e40c33525606d6c7c3775e6ba35f4ae30444fab735530eb3a03f66903d563e`

```dockerfile
```

-	Layers:
	-	`sha256:6d29117178a782b42058f2bb2da76af92811947cd2be7c43e83e3aa0939e5805`  
		Last Modified: Tue, 24 Dec 2024 22:37:06 GMT  
		Size: 7.3 MB (7293236 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:12f526139d82fdd73d6af1f9d6e5a2729ca4904c62e538056df4021e29155e3a`  
		Last Modified: Tue, 24 Dec 2024 22:37:06 GMT  
		Size: 14.2 KB (14242 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:96270f711b0180eda457c0c3732f5c353130b94c762d3e7cf69f9cb947f5b7aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.7 MB (231679639 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d4d3bffa905e0c83de37a74f9cb721e6296d777aeadfcf88959842f332cadde`
-	Default Command: `["clj"]`

```dockerfile
# Thu, 03 Oct 2024 17:49:34 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1733097600'
# Thu, 03 Oct 2024 17:49:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 03 Oct 2024 17:49:34 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Oct 2024 17:49:34 GMT
ENV CLOJURE_VERSION=1.12.0.1479
# Thu, 03 Oct 2024 17:49:34 GMT
WORKDIR /tmp
# Thu, 03 Oct 2024 17:49:34 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "94f29b9b66183bd58307c46fb561fd9e9148666bac13a4518a9931b6f989d830 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:82312fccb35f18983647c1ea71154b98ae9893fb61ca4febe12d584a3ea9ad6d`  
		Last Modified: Tue, 03 Dec 2024 01:29:57 GMT  
		Size: 48.3 MB (48325680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12adb99c50754583de50df89730f87bceb0ea5594a2c0eb741d28a13820617d6`  
		Last Modified: Tue, 03 Dec 2024 15:01:13 GMT  
		Size: 102.7 MB (102747746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0575a024f23f3e3068c4689116e9871da8ce9394f80a11fab72f59f0382d704c`  
		Last Modified: Tue, 03 Dec 2024 15:05:36 GMT  
		Size: 80.6 MB (80605567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4285b3158aa05103f6538094831265207bf4b41be6e7c9a63a904b8003af194e`  
		Last Modified: Tue, 03 Dec 2024 15:05:33 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:3a4e1c0a748b5f3cbef59c81f8fe5dab8a65a9025dac11e448588fd4348e0cd9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7324172 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce1c003c94390215c103db71afb6d609b95ce58e511eb467b23a5d1d56a3ac48`

```dockerfile
```

-	Layers:
	-	`sha256:eb4b2b34fc9d5318cb43a1f73de844ea69e4e6a9a2186018348be3ce68f50b83`  
		Last Modified: Tue, 03 Dec 2024 15:05:34 GMT  
		Size: 7.3 MB (7309812 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:336e9f3fea6259316bf32eb2d35dc2d9cacbe1dbc71d9c782ad3a98c9b069853`  
		Last Modified: Tue, 03 Dec 2024 15:05:33 GMT  
		Size: 14.4 KB (14360 bytes)  
		MIME: application/vnd.in-toto+json
