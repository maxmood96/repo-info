## `clojure:tools-deps-bullseye`

```console
$ docker pull clojure@sha256:53c28f2624f1e95503867845e44e5891063c8b9b5bd7ec0d7835fc294348d3e5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:tools-deps-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:a7b51ac5753e75248fc4ce21afc3a73310f22507196b925e45b4aefd45609be6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.8 MB (280800110 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e75a83ebab8d5c16379e92aeff9c62956ff55826d1fad2a42d57793f6a966599`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1749513600'
# Sat, 07 Jun 2025 17:38:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 07 Jun 2025 17:38:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 07 Jun 2025 17:38:11 GMT
ENV CLOJURE_VERSION=1.12.1.1550
# Sat, 07 Jun 2025 17:38:11 GMT
WORKDIR /tmp
# Sat, 07 Jun 2025 17:38:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "aea202cd0573d79fd8b7db1b608762645a8f93006a86bc817ec130bed1d9707d *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 07 Jun 2025 17:38:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:72049b7b8f2615e8b5167a09158b78d10a3b79a1ac60ce60cb5528a8c7723090`  
		Last Modified: Tue, 10 Jun 2025 23:24:16 GMT  
		Size: 53.8 MB (53754782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2922f207411efc1918b7759b6442495ca359cf027141047173a4dac1873466f`  
		Last Modified: Tue, 10 Jun 2025 23:52:32 GMT  
		Size: 157.6 MB (157634493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20821b454fbc8eab00129cac29e4a1c265092bd5930c91c247b7f29988b75630`  
		Last Modified: Tue, 10 Jun 2025 23:53:00 GMT  
		Size: 69.4 MB (69409797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2343d15689a01da751163ca09b2d5ecdb87f51976494d300d76c2d273e39717`  
		Last Modified: Tue, 10 Jun 2025 23:52:54 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac5f96434020fb1a1ec3684149a6d631c73a210b74c3dfc689f6c92854c8aaba`  
		Last Modified: Tue, 10 Jun 2025 23:52:55 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:fef614d6a8f625038a2b65534d6fbd6042263b2179184cf13181a9d09a5ba79e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7415912 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bac8072bb4fcee2ac25d5e880f5508a5df30878ee78915f71520dc165cc01fff`

```dockerfile
```

-	Layers:
	-	`sha256:6b4e981d3b9efe0f9ff4ea8e3d33ea20c89eb4ef6e1f2449ee3117ddd68e12f2`  
		Last Modified: Wed, 11 Jun 2025 03:38:26 GMT  
		Size: 7.4 MB (7399416 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9688d8973f1ec6d15e563cc85e44cace84ae59e59c52033866df32666964567e`  
		Last Modified: Wed, 11 Jun 2025 03:38:27 GMT  
		Size: 16.5 KB (16496 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:e75b1ec1425f0ecb40f7382d6e4fa75e1bf06a78c079f59e94d34ea6cb9433d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **277.7 MB (277719595 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43943bf4863f3dcab83f655bb5ff86de154ea63dab78efa29a13d224bfda1db5`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1749513600'
# Sat, 07 Jun 2025 17:38:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 07 Jun 2025 17:38:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 07 Jun 2025 17:38:11 GMT
ENV CLOJURE_VERSION=1.12.1.1550
# Sat, 07 Jun 2025 17:38:11 GMT
WORKDIR /tmp
# Sat, 07 Jun 2025 17:38:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "aea202cd0573d79fd8b7db1b608762645a8f93006a86bc817ec130bed1d9707d *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 07 Jun 2025 17:38:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:01b9f05048bbb73f25cf8fdb677f6390611ed20f4945645387ddce6122b5075e`  
		Last Modified: Tue, 10 Jun 2025 22:49:07 GMT  
		Size: 52.3 MB (52252301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc0dcb5ec9d5e14ecff4311df1937f52c510ad6d465139196e19d8c6d8e9f1ea`  
		Last Modified: Wed, 11 Jun 2025 08:34:01 GMT  
		Size: 155.9 MB (155928844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d78257653896b859f0dff555d488fa932e68828bc3174e9d098faef075d2499`  
		Last Modified: Wed, 11 Jun 2025 08:38:58 GMT  
		Size: 69.5 MB (69537415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fb1be1cc68135c7836ee785af2f6e0ec25b35a63e31e6462221397dc2b39ce1`  
		Last Modified: Wed, 11 Jun 2025 08:43:53 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8a20adb6342263aed8212dce7741768e2753c072fe4fd8b7efac3f25f9cdb12`  
		Last Modified: Wed, 11 Jun 2025 08:43:55 GMT  
		Size: 393.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:4c0877675ea29eef79d48014c110e0073fc5f6d6798cefa40412030dbf0314d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7421175 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b00177c6232ea0cc4cb21693e5a3eeabd2e6da2555d7069d0077be27b4a6f174`

```dockerfile
```

-	Layers:
	-	`sha256:0896e9bbbdc6a563e0121ca30b59a4a74b560b2da459bbad8522256ecad1adaf`  
		Last Modified: Wed, 11 Jun 2025 09:39:30 GMT  
		Size: 7.4 MB (7404539 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cf5118b2910e3614baafb3703a9c944220d6d4e12507214c159f5fd0aa62cc43`  
		Last Modified: Wed, 11 Jun 2025 09:39:30 GMT  
		Size: 16.6 KB (16636 bytes)  
		MIME: application/vnd.in-toto+json
