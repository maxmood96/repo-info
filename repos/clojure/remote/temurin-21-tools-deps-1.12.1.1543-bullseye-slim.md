## `clojure:temurin-21-tools-deps-1.12.1.1543-bullseye-slim`

```console
$ docker pull clojure@sha256:f59925616d4bfb58c5516b8b639ffb6254160138a1962a523b75e69842577e29
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-21-tools-deps-1.12.1.1543-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:005ca3913064d6a3b4bbfc6ad2054fabc3b831b8e4dfacf7d84722dec35ffc4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.9 MB (246897385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64e46eb5ecf7c17aa07206c8f9444048e86ebf39eed48eea5b157c59a5c66314`
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
	-	`sha256:03af077612f84a578bdbdb482d2afb41dccce23b628e7d5da92d969b9e38eda5`  
		Last Modified: Tue, 03 Jun 2025 18:24:15 GMT  
		Size: 157.6 MB (157634503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:591b91b54266290e67e1a9fd317209156dc9cf63cabfa6629ee2e6f68b1cf8d4`  
		Last Modified: Tue, 03 Jun 2025 18:24:14 GMT  
		Size: 59.0 MB (59005903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04586adda0d266910ce3b91b3692c6f8440d75ede9a1374ffead9dbd1d76f4d8`  
		Last Modified: Tue, 03 Jun 2025 18:29:50 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d76604668873fe5d090476c36f4f67612e813a075e15c3dbada12580da19725`  
		Last Modified: Tue, 03 Jun 2025 18:29:54 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.1.1543-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:27343d0442b0a1515c355a367957d1a85c4c8e3f0469b902ea9cb5006fcc8ebd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5188959 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b2621bad897ef1801407a30e5c94b3de0793c2ea0087b5b68124874f0430661`

```dockerfile
```

-	Layers:
	-	`sha256:87dc0357dfd1e7c69bae13f6af450b8b5308829ba803b7563e5770a1d2d01834`  
		Last Modified: Tue, 03 Jun 2025 18:38:55 GMT  
		Size: 5.2 MB (5172384 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d5161b8a1693541bdb290dfeee8d1ad4253d769b5619e40ca102198c0d1157e3`  
		Last Modified: Tue, 03 Jun 2025 18:38:56 GMT  
		Size: 16.6 KB (16575 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-1.12.1.1543-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:25e555039604ba6f5fb2c745224c789c9e11a342251821c98364f01bd117460e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.8 MB (243813918 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cde2311135d35d6ee9655fe1bc31f2003e6e4b0d3372254b68aca2db0e4de2cb`
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
	-	`sha256:85c27f9d6798235ccf5e5f695d350773cf03adc77fea3cfc1049c69b79bf7dba`  
		Last Modified: Tue, 03 Jun 2025 13:32:50 GMT  
		Size: 155.9 MB (155928816 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15bdb3acd3d19eb2b0328cfadd54c2f23bb254ac95e197405777dafd108914ff`  
		Last Modified: Tue, 03 Jun 2025 18:48:06 GMT  
		Size: 59.1 MB (59137806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92825935ccad31792068483c29aff241d47cebb55ed54de500c50a739ef9f25d`  
		Last Modified: Tue, 03 Jun 2025 18:48:01 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0eb91f8b8aa055f5474befdf5c491c9f3d04ed204f8225682568851a0fd10750`  
		Last Modified: Tue, 03 Jun 2025 18:48:01 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.1.1543-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:ef5b22d3ff2ee53ee7810511440d91906f089514d2dad36446b8bd6f70d222f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5194856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f793cf4c59d637841161361361982c5ee37d42fa2782526b8aa0d96471377f2`

```dockerfile
```

-	Layers:
	-	`sha256:f309447b12f49a5d125db4a94f721b908ba118f551ca0cc82d65b166ce176bfc`  
		Last Modified: Tue, 03 Jun 2025 21:40:09 GMT  
		Size: 5.2 MB (5178140 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1af086611c445c78d717a6e86ef6fc72087bdb08d22d10dee7a0716f7dea2a99`  
		Last Modified: Tue, 03 Jun 2025 21:40:10 GMT  
		Size: 16.7 KB (16716 bytes)  
		MIME: application/vnd.in-toto+json
