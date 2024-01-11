## `clojure:temurin-11-bullseye-slim`

```console
$ docker pull clojure@sha256:1cc6b3d01d5096769fefa731bb00ccbddf486c18dd8bd782fe8cd504db5a705f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-11-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:276f56db2aae4fabda6a6f23783a69f3a90e554223ca0ad2fec914625ed4a766
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.3 MB (235314559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c9afa69a0dad6f3a8b498a27c04cc5e7104b474e2aac32fa8b48a1d63fdd057`
-	Default Command: `["clj"]`

```dockerfile
# Thu, 11 Jan 2024 02:38:16 GMT
ADD file:bd961ef3fd78ceb8ce13f43a6b265e2bef640dfff887462b8ceb73a1d4637401 in / 
# Thu, 11 Jan 2024 02:38:17 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 04:53:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Jan 2024 04:59:46 GMT
COPY dir:7cbebf37ba11e5c859b49d766118c0899546d922ac426dfa1230f08ebde784dc in /opt/java/openjdk 
# Thu, 11 Jan 2024 04:59:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jan 2024 05:03:15 GMT
ENV CLOJURE_VERSION=1.11.1.1435
# Thu, 11 Jan 2024 05:03:15 GMT
WORKDIR /tmp
# Thu, 11 Jan 2024 05:03:32 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "7edee5b12197a2dbe6338e672b109b18164cde84bea1f049ceceed41fc4dd10a *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Thu, 11 Jan 2024 05:03:33 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Thu, 11 Jan 2024 05:03:33 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:0e0969fcaa8240e1eeb53f9f5d4ddd1bf89a2c9971c9cbe455eba0e66eeefb53`  
		Last Modified: Thu, 11 Jan 2024 02:43:09 GMT  
		Size: 31.4 MB (31417955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67b73066ba82716b83b2f778c5be1f8d952d9952a3fe0c473dea2bf497f35bbb`  
		Last Modified: Thu, 11 Jan 2024 05:18:40 GMT  
		Size: 145.3 MB (145266337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b55fb4a9c268cc170742a32cc2e7f3ef995a27c57c4fb72bfe89719fc9e9566b`  
		Last Modified: Thu, 11 Jan 2024 05:20:42 GMT  
		Size: 58.6 MB (58629651 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5779af581381391c8e7f7b69160da35392affd375aff4aee3cb0f2904e14195e`  
		Last Modified: Thu, 11 Jan 2024 05:20:35 GMT  
		Size: 616.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-11-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:4044440c9ebea42e38867308da3f6a075020848e0ac8c6550da628aa777b746e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.8 MB (230822843 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f6a6997ae40e329f03c131f2baabd1cea98d7149bb8c6e2525f524a1ef2d4ae`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 19 Dec 2023 01:41:25 GMT
ADD file:4dd1c5e17a5e57644787f37e8ad290baef6c93f4f112b976f19136480a293713 in / 
# Tue, 19 Dec 2023 01:41:25 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 03:00:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 19 Dec 2023 03:01:51 GMT
COPY dir:679954ac595f0d76b401a9a7d1ae039330e7231cb1c29892d5f56a0e84534783 in /opt/java/openjdk 
# Tue, 19 Dec 2023 07:00:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Jan 2024 20:46:04 GMT
ENV CLOJURE_VERSION=1.11.1.1435
# Thu, 04 Jan 2024 20:46:04 GMT
WORKDIR /tmp
# Thu, 04 Jan 2024 20:46:18 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "7edee5b12197a2dbe6338e672b109b18164cde84bea1f049ceceed41fc4dd10a *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Thu, 04 Jan 2024 20:46:19 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Thu, 04 Jan 2024 20:46:19 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:2244706f264b35566276550fbc21ada79613ddfff850e372b8f5113110a67c93`  
		Last Modified: Tue, 19 Dec 2023 01:45:22 GMT  
		Size: 30.1 MB (30064052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc9b17def4f28a4c890f414b976902690074fb9a259e92623f2bce7129f95d48`  
		Last Modified: Tue, 19 Dec 2023 03:04:57 GMT  
		Size: 142.0 MB (142001838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:227e2a0aa09dc5f9710a9107be77041d43dcfcd7ac347faca6ce2b0fdfb15f88`  
		Last Modified: Thu, 04 Jan 2024 20:56:18 GMT  
		Size: 58.8 MB (58756335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ce5a2701541233417621f7a86e3ea9c7fb8dcad852fdff84fe11fb174e2a2db`  
		Last Modified: Thu, 04 Jan 2024 20:56:11 GMT  
		Size: 618.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
