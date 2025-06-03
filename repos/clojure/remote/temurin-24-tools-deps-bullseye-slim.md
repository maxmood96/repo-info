## `clojure:temurin-24-tools-deps-bullseye-slim`

```console
$ docker pull clojure@sha256:2a78db4651d2228286477d2671cb5fee44c39e8c43b446395d63c797256d8b4d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-24-tools-deps-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:7d1a366d6c83cf6ecc84d27d1b8c3215245179c037cf86d453d9ce56715b3dd7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.2 MB (179214752 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f3b6ea435056ae2d6724e6a2d660969413252553c67baa9e30917f97219a746`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1747699200'
# Tue, 03 Jun 2025 15:45:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Jun 2025 15:45:26 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Jun 2025 15:45:26 GMT
ENV CLOJURE_VERSION=1.12.1.1543
# Tue, 03 Jun 2025 15:45:26 GMT
WORKDIR /tmp
# Tue, 03 Jun 2025 15:45:26 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "09b7b8185b8a35b1ddcc9c2a5155d094fe1237805c24489312f3e324a83b0d4c *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 03 Jun 2025 15:45:26 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:e1f16b66c2e86ad38458eba597e4ec79e4750398a28dbbc2d7819d829c4c9023`  
		Last Modified: Tue, 03 Jun 2025 13:30:16 GMT  
		Size: 30.3 MB (30255940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46333678e4802929bc4af8d183fb0196cbf39e16758bc3a263cd44cb4b2719f7`  
		Last Modified: Tue, 03 Jun 2025 18:25:06 GMT  
		Size: 90.0 MB (89952003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aedffe6c044d3b6063f12d0d7425d15133da8d7586b0688aa62abf2376ed6871`  
		Last Modified: Tue, 03 Jun 2025 18:25:04 GMT  
		Size: 59.0 MB (59005768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f9410294a4dab16abbd5ebe4c2b61d4d76f0808b2e7baec3e3a485925a473d1`  
		Last Modified: Tue, 03 Jun 2025 18:25:00 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e0105630dc59f930d265b27d87ac48dc989f8a9f6bc38818e9cefa753f34dfe`  
		Last Modified: Tue, 03 Jun 2025 18:25:01 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-tools-deps-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:bf68a5a2a9a99771ae7afa0d298e26cd32814563a7ce9f7c66fed90f98f3d21c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5135102 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdb292cf90f5d8ab7425acb34176d4bfd267adecfaf1bb36d982a399aa587090`

```dockerfile
```

-	Layers:
	-	`sha256:478763fa3f55fdb2550d2b6f6949f4b195ddae42c79548b835c9690120412f9f`  
		Last Modified: Tue, 03 Jun 2025 21:42:41 GMT  
		Size: 5.1 MB (5119232 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b5aadd094fff728f91fc032759278183ab613c4f347d1519e99fa0a1b9fc9580`  
		Last Modified: Tue, 03 Jun 2025 21:42:42 GMT  
		Size: 15.9 KB (15870 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-tools-deps-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:466a594536d0f2005ec95bbc84893ff4ea8512a821515cf98388317db897c20a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.0 MB (176976201 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ff5264542e172702e0b02e0ca7096a453188119d8d5ed9c7c7fbd3607cb670c`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1747699200'
# Tue, 03 Jun 2025 15:45:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Jun 2025 15:45:26 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Jun 2025 15:45:26 GMT
ENV CLOJURE_VERSION=1.12.1.1543
# Tue, 03 Jun 2025 15:45:26 GMT
WORKDIR /tmp
# Tue, 03 Jun 2025 15:45:26 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "09b7b8185b8a35b1ddcc9c2a5155d094fe1237805c24489312f3e324a83b0d4c *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 03 Jun 2025 15:45:26 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:66850c8b65c1e9c3674a722b71f8887dd317a9b257148bb1063e88d85790544f`  
		Last Modified: Tue, 03 Jun 2025 13:30:45 GMT  
		Size: 28.7 MB (28746257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bded46ee81e89e59e64c533c353440bea9d4be7e5e0f2def77398507b60fd0f`  
		Last Modified: Tue, 03 Jun 2025 21:26:27 GMT  
		Size: 89.1 MB (89091274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52ab2aaa0fa80d7ed454883a05e580e69557fb7c40daed731372931206965749`  
		Last Modified: Tue, 03 Jun 2025 18:54:48 GMT  
		Size: 59.1 MB (59137628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14f72905b49029f932a2ddb4d7ad7d17456c52de9f46b00c1ab0ddf64458eaf6`  
		Last Modified: Tue, 03 Jun 2025 18:54:42 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba8cc6e1876419eb2d634796d85b30240a36613a2c90895d3a62433d73336b5b`  
		Last Modified: Tue, 03 Jun 2025 18:54:44 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-tools-deps-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:27c61b6ab0bbe8cb088a92a5e2fc3894e05258bca6b91279578b1349d3799ea3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5140951 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a39e935a023919d1b16bf19902092d8d5d7741a3b17a1d98419be178313501ac`

```dockerfile
```

-	Layers:
	-	`sha256:51b829be40e5e32508cee5f9625275f521d598dcd3fd7803ec06e8c7aa16d016`  
		Last Modified: Tue, 03 Jun 2025 21:42:46 GMT  
		Size: 5.1 MB (5124961 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8b58162ffd7de8676c2e86cdf0613d6f23462c62079bfa5f39a078171d1fac52`  
		Last Modified: Tue, 03 Jun 2025 21:42:47 GMT  
		Size: 16.0 KB (15990 bytes)  
		MIME: application/vnd.in-toto+json
