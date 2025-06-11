## `clojure:temurin-21-tools-deps-1.12.1.1550-bullseye`

```console
$ docker pull clojure@sha256:50d4080d305840e0c9e982a20100da6099f99d957e78750d9629e210f047652a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-21-tools-deps-1.12.1.1550-bullseye` - linux; amd64

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

### `clojure:temurin-21-tools-deps-1.12.1.1550-bullseye` - unknown; unknown

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

### `clojure:temurin-21-tools-deps-1.12.1.1550-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:b41c183edfa628df2577e3421c15df65d6caa94fc42c2a7f26bec37f7e53f4f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **277.7 MB (277715487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48f4b58c4b7a48b30cad5c5759d059e59e62e27abb96d91d597f7e6c7bb649d7`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1747699200'
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
	-	`sha256:b2737025fe8da5b868f566cb4e3dc3330028cee06c83db854f56467eca6e09b8`  
		Last Modified: Tue, 03 Jun 2025 13:30:20 GMT  
		Size: 52.2 MB (52247755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34a5e26e3cb5abfbd307a69d846765430705dd9214f5910e9a937311871d3dc9`  
		Last Modified: Wed, 04 Jun 2025 12:44:46 GMT  
		Size: 155.9 MB (155928831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da4f8352ceba8fc0b8d3c4194bb0aa338dbdced1d51b9d2086648ca13db4980a`  
		Last Modified: Mon, 09 Jun 2025 18:59:03 GMT  
		Size: 69.5 MB (69537859 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a235369774b1893ac10b7bb4772c9de399687f197cccc773f5849c11421ea25`  
		Last Modified: Mon, 09 Jun 2025 18:00:26 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:921123a56dd14c85e220aa9939ff184240c5946503d3f265191280a5e829ef95`  
		Last Modified: Mon, 09 Jun 2025 18:00:30 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.1.1550-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:32459af2cbabfbac8f6342723118a36bf96edb78320fb2cee13018e4db04f9cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7422802 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:550995c2abbd329e42bb1e01557a5392c08915d3ffc3bc71699406492cdff450`

```dockerfile
```

-	Layers:
	-	`sha256:f98039738ec2a03b7c234d1cc2fb57f27353be158feb6f6483704643f105841a`  
		Last Modified: Mon, 09 Jun 2025 18:39:17 GMT  
		Size: 7.4 MB (7406163 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:89ed8f3e8a73e6230f802a6326172ca416669208262819374d1093e1290ab92e`  
		Last Modified: Mon, 09 Jun 2025 18:39:18 GMT  
		Size: 16.6 KB (16639 bytes)  
		MIME: application/vnd.in-toto+json
