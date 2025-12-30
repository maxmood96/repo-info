## `clojure:temurin-11-tools-deps-1.12.4.1582-bullseye-slim`

```console
$ docker pull clojure@sha256:8329b20bcca7664b157f5cb22a35f678b4bde1b75a63ffb0163918be7fdd781d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-tools-deps-1.12.4.1582-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:89b3cef074e9fcc4c1c81e2bb2747973db55c7bb028d3dfbe1f0387a9a40fac3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.4 MB (234375727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26d31f828e3ca41abe911b56bb11b26199bdd31ec97dffbe6b5b897ea3f5d79b`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1766966400'
# Mon, 29 Dec 2025 23:58:25 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 29 Dec 2025 23:58:25 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 29 Dec 2025 23:58:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 29 Dec 2025 23:58:25 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Tue, 30 Dec 2025 00:56:29 GMT
WORKDIR /tmp
# Tue, 30 Dec 2025 00:56:42 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 30 Dec 2025 00:56:42 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 30 Dec 2025 00:56:42 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:37b52eae712b138ea3c9639c687f975153ccba96801de3dc69883975843edb35`  
		Last Modified: Mon, 29 Dec 2025 22:27:47 GMT  
		Size: 30.3 MB (30258441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:101a925c630cbaf9c1eb0c63a2a98fa6fe7b294efe3baab6de6db13ffc477feb`  
		Last Modified: Mon, 29 Dec 2025 23:59:34 GMT  
		Size: 145.0 MB (144966652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67d025ba9c755bc0fa872da9c2cf13b55d3648e22fcf52f351c56c316f782aca`  
		Last Modified: Tue, 30 Dec 2025 00:57:18 GMT  
		Size: 59.1 MB (59149991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eefc4f8b7758a8868a2a2238d6f8b78586559d06a242a0691f7e2e73662a5b9b`  
		Last Modified: Tue, 30 Dec 2025 00:57:03 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.4.1582-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:8ac510af40c9ad526fd4dd7b18a4afe9be0b754cbc09e98139be6673b3ae34c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5341673 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:646c6b6c96eda74bd76d75b188d5032cde69342ed04571ae62d2a4270d4cd35d`

```dockerfile
```

-	Layers:
	-	`sha256:812bb38ebe5b52addf22a1d45c128076444c62596bba9e562b950faf2d528fa1`  
		Last Modified: Tue, 30 Dec 2025 04:37:08 GMT  
		Size: 5.3 MB (5328208 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0490e3808072b4750ffd1402fafc65b672894603be7a0968ff0c736bb49c409f`  
		Last Modified: Tue, 30 Dec 2025 04:37:08 GMT  
		Size: 13.5 KB (13465 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-1.12.4.1582-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:0b87c19560f5a006cc9efa3b31aec862da26483b9cf7975a03feaec5c106ab8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.8 MB (229765061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ed53a6c3d9d56b07441920adfb53074d14d514742ba1bc245da0226e508191e`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1766966400'
# Tue, 30 Dec 2025 00:57:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 30 Dec 2025 00:57:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 30 Dec 2025 00:57:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Dec 2025 00:57:36 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Tue, 30 Dec 2025 00:57:36 GMT
WORKDIR /tmp
# Tue, 30 Dec 2025 00:57:50 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 30 Dec 2025 00:57:50 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 30 Dec 2025 00:57:50 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:2b952d66bc8c719b5ca92eacb4307075591731bdc405a12ebd6fa840a24375b7`  
		Last Modified: Mon, 29 Dec 2025 22:27:18 GMT  
		Size: 28.7 MB (28748462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48872ca889428be28cf6f01c19cb518488e3b3a4de2f7a06d648f26f3a18bef0`  
		Last Modified: Tue, 30 Dec 2025 00:58:29 GMT  
		Size: 141.7 MB (141731575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65b51c9970dda15f9cc8627185a5b341a40fbbd2cc05b6602fb90d6bb37ded2b`  
		Last Modified: Tue, 30 Dec 2025 00:58:23 GMT  
		Size: 59.3 MB (59284378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7234776d46d91125959e78e01af318d8a4344cb7ce8e9cad5bd083568e938a02`  
		Last Modified: Tue, 30 Dec 2025 00:58:17 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.4.1582-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:a671b726d9218f61d10e48da856ef7a5acfa5630add964a4f8c4ec7d1f812446
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5348943 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f1816adc8f0a5ce765ac8ba31893b69c0f4e0ddfe03e76503dfd8ec652b239d`

```dockerfile
```

-	Layers:
	-	`sha256:6c685ed4ebe2cba2aa0df2eb23f7f665ee754f929a20ecfc350aec90625d2fcb`  
		Last Modified: Tue, 30 Dec 2025 01:35:28 GMT  
		Size: 5.3 MB (5334558 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:474a2ad98653b3ca429a559417cb1aabf301cbccd4d49ac801fd88ab5886d254`  
		Last Modified: Tue, 30 Dec 2025 01:35:29 GMT  
		Size: 14.4 KB (14385 bytes)  
		MIME: application/vnd.in-toto+json
