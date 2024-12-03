## `clojure:temurin-8-tools-deps-bookworm`

```console
$ docker pull clojure@sha256:effdf333fff4f71ce3c27393d84758e88db623fd05461458cd954195753eb837
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:5352587daacc53ebe7ec440dfc6cde430af3af75f4646d5fdc5c850e94244a84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.9 MB (232876097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6964db4bd9eda58c443c14d4741338e7d68cf2a37037ea56087326a5e0bab18`
-	Default Command: `["clj"]`

```dockerfile
# Thu, 03 Oct 2024 17:49:34 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1733097600'
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
	-	`sha256:fdf894e782a221820acf469d425b802be26aedb5e5d26ea80a650ff6a974d488`  
		Last Modified: Tue, 03 Dec 2024 01:27:13 GMT  
		Size: 48.5 MB (48497210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d46afd374d1f5883e7fac7dbc3c08e8ad4ed34400bf285a382735561528bb976`  
		Last Modified: Tue, 03 Dec 2024 03:19:25 GMT  
		Size: 103.6 MB (103633923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cd60a82602ac3561a02627c6ba3d5b3355a177e4c6d63b8e5564c8502bd2b93`  
		Last Modified: Tue, 03 Dec 2024 03:19:25 GMT  
		Size: 80.7 MB (80744320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e2986535e01aa9cd9bbea9af281829f44f7f15fe85ae096106420e20137c2e8`  
		Last Modified: Tue, 03 Dec 2024 03:19:23 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:18406002dc24d6511fb729a6dba60ac215e9d4314772f7d38af1426e00c1c631
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7317586 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a10f5faf034b73b12e9bdc149431898ebea7ca2ba5ceabebd4b76e45c1eaa6eb`

```dockerfile
```

-	Layers:
	-	`sha256:69e12e72f35e850b2a8dec3c11bb21efe8dd149f9bcf04df8531198b68b687b7`  
		Last Modified: Tue, 03 Dec 2024 03:19:24 GMT  
		Size: 7.3 MB (7303345 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3b44ec66afbf5fbf1d30838e21dae1baa71363279787642b9b15d1a098eff496`  
		Last Modified: Tue, 03 Dec 2024 03:19:23 GMT  
		Size: 14.2 KB (14241 bytes)  
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
