## `clojure:tools-deps-1.12.0.1530`

```console
$ docker pull clojure@sha256:e30c2b7f3be4a43350b531d4ea1df9b654f263c452c16e8322c7c4ecfb4a12ed
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `clojure:tools-deps-1.12.0.1530` - linux; amd64

```console
$ docker pull clojure@sha256:43f0064f1f6c17b2cbabfeea34fcd5ce0eef724b78cc673b05d269aea9b5db9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.1 MB (287055944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2155f7da82c91f89ee70323d0fd8a9d2714cc321a8e5d2f19d1a3e1e116407f`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 24 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1740355200'
# Sat, 08 Mar 2025 19:45:48 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Mar 2025 19:45:48 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 08 Mar 2025 19:45:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Mar 2025 19:45:48 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Sat, 08 Mar 2025 19:45:48 GMT
WORKDIR /tmp
# Sat, 08 Mar 2025 19:45:48 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 08 Mar 2025 19:45:48 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 08 Mar 2025 19:45:48 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 08 Mar 2025 19:45:48 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 08 Mar 2025 19:45:48 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:155ad54a8b2812a0ec559ff82c0c6f0f0dddb337a226b11879f09e15f67b69fc`  
		Last Modified: Tue, 25 Feb 2025 01:29:36 GMT  
		Size: 48.5 MB (48476100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6d1d582b85c2376bbd182918cb5820da4eb2712fea9d1bcb36abbdcbddd86eb`  
		Last Modified: Mon, 10 Mar 2025 17:40:12 GMT  
		Size: 157.6 MB (157585931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf37b77836b3c643fac976dd2fb94a8123b50f9f635c52ea147fb3687932c778`  
		Last Modified: Mon, 10 Mar 2025 17:40:11 GMT  
		Size: 81.0 MB (80992870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03b5789ee6f2ceac5355a4d5820e658d047ae8c466c654112c04317ad95056d9`  
		Last Modified: Mon, 10 Mar 2025 17:40:10 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f9a6fa88f2b4b58ebea5c4cdb6984c9827bf85a96823d36e9f0ce659693f4ec`  
		Last Modified: Mon, 10 Mar 2025 17:40:10 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.12.0.1530` - unknown; unknown

```console
$ docker pull clojure@sha256:5bbd810b60d9e9dc70df226fbf27e85edec1d78cfa4183f5b66cc2e4c6f63cb4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7194019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48f21ca68a0d6e445184a6c7b9e1374eedab309384973ab512b23df9fe6bcad1`

```dockerfile
```

-	Layers:
	-	`sha256:03118f34de1d6b494d9e449b4e9ae8cec120fd62da6de1323f4a2fb783dab6d8`  
		Last Modified: Mon, 10 Mar 2025 17:40:10 GMT  
		Size: 7.2 MB (7176198 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cb40f89558477ae703d3ec5a3cb1e16663ca9814f4b0a2c0cfb60b1448a2d44d`  
		Last Modified: Mon, 10 Mar 2025 17:40:10 GMT  
		Size: 17.8 KB (17821 bytes)  
		MIME: application/vnd.in-toto+json
