## `clojure:temurin-17-tools-deps-1.12.0.1530-bullseye-slim`

```console
$ docker pull clojure@sha256:02e8beadad5f4ebd89be868b4b14c021da8658492d742c3458f13592261418c0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-tools-deps-1.12.0.1530-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:08ffdc2f011f883a4c899c18f86d2e4ae3d7e137e73c618b9614785bc08031aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.9 MB (233883588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df19048c227a29d094863ed88a0cd27619ca3c5d2309f80874f5194fad7bbcd2`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1745798400'
# Mon, 28 Apr 2025 17:24:54 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 28 Apr 2025 17:24:54 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 28 Apr 2025 17:24:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 28 Apr 2025 17:24:54 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Mon, 28 Apr 2025 17:24:54 GMT
WORKDIR /tmp
# Mon, 28 Apr 2025 17:24:54 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 28 Apr 2025 17:24:54 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 28 Apr 2025 17:24:54 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 28 Apr 2025 17:24:54 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 28 Apr 2025 17:24:54 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:c8e1eb8ab3b017bd9e33ddec83ebdd8292c542bbd14a8d5a6cfa2edc3ad3b8eb`  
		Last Modified: Mon, 28 Apr 2025 21:08:07 GMT  
		Size: 30.3 MB (30254604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64605cff81b40473d8f25896ec2723ba277d28b3ce896766fbb1321c6c2c7f69`  
		Last Modified: Mon, 28 Apr 2025 22:07:32 GMT  
		Size: 144.6 MB (144634946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fcdf2bc0df5a28f1e3e2975fc8c8f6cf16cb8f9b1dee9b66e5a81aa8fe4ef7d`  
		Last Modified: Mon, 28 Apr 2025 22:07:31 GMT  
		Size: 59.0 MB (58992998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f963ce4a357023d3ac80219020c9a1cf7ef0156275b058ec55a83780280006e`  
		Last Modified: Mon, 28 Apr 2025 22:07:30 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a21f5afcd69ec7c3752023c5a1c518fe127adc91a3c95cb123090cc116adc26b`  
		Last Modified: Mon, 28 Apr 2025 22:07:30 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.0.1530-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:9f7f89a61b9162356575a564a732c1175fd9ee9fc4c4a794796a30b138b1bc61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5134944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a09159c9ab2330f171167cb5666dcb7259cbbb17135ab83d1069af1d00177131`

```dockerfile
```

-	Layers:
	-	`sha256:df9c5908db7030fb75fe174170b5718e6ede229f4e165eb479ad7da640fd45b8`  
		Last Modified: Mon, 28 Apr 2025 22:07:30 GMT  
		Size: 5.1 MB (5119067 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:96aa38c2f67cd0c825ee0e55c7d12dbaba94f556fee458149b9cd78e0643aeab`  
		Last Modified: Mon, 28 Apr 2025 22:07:30 GMT  
		Size: 15.9 KB (15877 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.0.1530-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:edf879da1e870f59daf270d624ed9f3baf3a3077ba6679a402ce6d710d565ee6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.4 MB (231385716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebeb2ef797d3d11cf7258e6efe6df9b2ba59eb571eba340ed6b19fdea78410f4`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1745798400'
# Mon, 28 Apr 2025 17:24:54 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 28 Apr 2025 17:24:54 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 28 Apr 2025 17:24:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 28 Apr 2025 17:24:54 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Mon, 28 Apr 2025 17:24:54 GMT
WORKDIR /tmp
# Mon, 28 Apr 2025 17:24:54 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 28 Apr 2025 17:24:54 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 28 Apr 2025 17:24:54 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 28 Apr 2025 17:24:54 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 28 Apr 2025 17:24:54 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:5d3a81360c5bb9281a4f735a1468429a1898f1a4fc24a2581dde4cf28ace4488`  
		Last Modified: Mon, 28 Apr 2025 21:21:09 GMT  
		Size: 28.7 MB (28744645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d72262fe32b026e7f23e9a38bfb2a66973be30355ac7b2a0fe73a91bfb575d0f`  
		Last Modified: Tue, 29 Apr 2025 20:15:14 GMT  
		Size: 143.5 MB (143512633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba0e19b5e3394bc095f8ad5c27d5c5e1c3fd22b4f6cd80b767e30c4aeeafc227`  
		Last Modified: Wed, 30 Apr 2025 01:35:49 GMT  
		Size: 59.1 MB (59127401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:254e0548c3b863fc08614dbe860fdd2fc9bd6df7bc66e74b6161d816eef40680`  
		Last Modified: Wed, 30 Apr 2025 01:35:47 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a429f73077911a0c66230a5e31b6a230afea1fb6be9b70c1a51ad0dc0658b580`  
		Last Modified: Wed, 30 Apr 2025 01:35:47 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.0.1530-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:a808735d0085e0ee1d59a020d4b64112cd6c9db272f5339d4cb8923800567054
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5140796 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77b302d681ec091dc9c289025aeba7a10cbab2e20726c51609c24f3a1508c442`

```dockerfile
```

-	Layers:
	-	`sha256:5e37b241d0f0a1e98a24ef6da0ad8f7d048dde6d2c710d69a2c5a66faf5ef57c`  
		Last Modified: Wed, 30 Apr 2025 01:35:47 GMT  
		Size: 5.1 MB (5124799 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b297d6956fe648b368f3cc30687c20d8b631cf4c1823cf062e74ac2b35e6ba9a`  
		Last Modified: Wed, 30 Apr 2025 01:35:46 GMT  
		Size: 16.0 KB (15997 bytes)  
		MIME: application/vnd.in-toto+json
