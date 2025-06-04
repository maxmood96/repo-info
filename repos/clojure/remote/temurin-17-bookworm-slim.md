## `clojure:temurin-17-bookworm-slim`

```console
$ docker pull clojure@sha256:ee779e93ceecbca98d8779f8e0f675e7d1daeed1e0fce8d19b3f73551d17b16c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `clojure:temurin-17-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:3b5b3129d412f2cec1bfc2c2e4636d8a98947d029ba0c233d55fff9f35796cfc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.4 MB (242390831 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66dbdf169faf6d692935c46749537348dfd13842c78901b319e0bf277412a29d`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1747699200'
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
	-	`sha256:61320b01ae5e0798393ef25f2dc72faf43703e60ba089b07d7170acbabbf8f62`  
		Last Modified: Tue, 03 Jun 2025 13:30:15 GMT  
		Size: 28.2 MB (28225330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64a6701e918f1b704d1082f4155a6efb06ab33f1780d1b6ab5c1cc1386c0b578`  
		Last Modified: Wed, 04 Jun 2025 03:03:57 GMT  
		Size: 144.6 MB (144635069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0982c1ffd57d058a7370c6d9c0844c19cb2a848f4bc34bf4f7ff8a68ede1984a`  
		Last Modified: Wed, 04 Jun 2025 03:03:52 GMT  
		Size: 69.5 MB (69529392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23822d33e579650e726bd9bf035a369fa9c1870c35321680f02da4c8334b8862`  
		Last Modified: Wed, 04 Jun 2025 03:03:49 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3e5540663f5bcb296decde04d8087d7450eca0ed0bf73ca0ed331538f97f942`  
		Last Modified: Wed, 04 Jun 2025 03:03:50 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:ef86ad2bcf13f763b2e20b266096f162df8999e0cafc174de72aba0ea6958e5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4977377 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e93a959df09b82f097ee7cce557dd7257e0282434b9ab568261619b3b39d17a`

```dockerfile
```

-	Layers:
	-	`sha256:7d9eb1f1d6ec44b4c05ee547aaae98ad0c17b907ffc8f120648aad9e56bd6368`  
		Last Modified: Tue, 03 Jun 2025 21:37:27 GMT  
		Size: 5.0 MB (4961498 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9764aa0ae0bbfb8245ebf0f2ffc8b9a3f0679aba4d69aa4f4473994340ff099a`  
		Last Modified: Tue, 03 Jun 2025 21:37:28 GMT  
		Size: 15.9 KB (15879 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:a98b6aef66ba06cc530d7341f6e8c37883825a43cc3b777d2c8d44ef4598f85e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.0 MB (240970771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:041e242a1684d9a24ace8f4398f189123a1745187340eba718151fff12d11071`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1747699200'
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
	-	`sha256:b16f1b16678093d11ecfece1004207a40f9bc1b7d9d1d16a070c1db552038818`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 28.1 MB (28065280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccbfa317a80df2e7dc3da8da387d9081ffa13f5e29daff53d5dcef29b40af4a3`  
		Last Modified: Tue, 03 Jun 2025 12:46:25 GMT  
		Size: 143.5 MB (143512643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d77031fe264e8e0c43b4f4297e93cafab447487ef04be92ddbfaabb6a8bfdf21`  
		Last Modified: Tue, 03 Jun 2025 18:39:49 GMT  
		Size: 69.4 MB (69391809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5fd29c3c646d5262f2181c6346eb4b5caf78825ceafbc0d3fb055a818037002`  
		Last Modified: Tue, 03 Jun 2025 18:39:27 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36c58d5d1ff3a0adaaa157f8ecd6176271ca9f9eec17d96aad6f2c2a598753e8`  
		Last Modified: Tue, 03 Jun 2025 18:39:28 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:ad486375c6035583ff50bc2d0930d8bb1e4748c118f0f207b52eb385c1bc495c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4983256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e45dd45b45130c5ddd60d19eabb087d1d64d6b0843d1ba81423302faf6a64c4c`

```dockerfile
```

-	Layers:
	-	`sha256:42ebf43eb419b8948b3d4590635561ccfde3b07b1d5bbd7c17d9adbe6806e081`  
		Last Modified: Tue, 03 Jun 2025 21:37:32 GMT  
		Size: 5.0 MB (4967259 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a34285c245a03f2cf292b1f14dc65e51c3001612c511ef8140f0a6fc9c7c8baa`  
		Last Modified: Tue, 03 Jun 2025 21:37:33 GMT  
		Size: 16.0 KB (15997 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:0b4712ac74a44d33384d2dc724a7733c92d92d0ea88bb1ae81b041932adc0145
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **251.7 MB (251694078 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91e23c4df52986cf16b18bbb0e28cebcb3b3d43b24b87a5c6ac3d90d1eb7390a`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1747699200'
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
	-	`sha256:701606535a7233566815cc9ad5f3e5853b443be5476286f6799008053dc2b03b`  
		Last Modified: Tue, 03 Jun 2025 13:39:02 GMT  
		Size: 32.1 MB (32066912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07686e6fdd26baa61178aa1b8e90f5239ab4c91006e539b5fbf39feb82e0a434`  
		Last Modified: Tue, 03 Jun 2025 08:46:31 GMT  
		Size: 144.3 MB (144280562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4268f03ce853d153da4aac3245431b56456d181ae6fe607eec80fad0adae1f4b`  
		Last Modified: Tue, 03 Jun 2025 18:51:23 GMT  
		Size: 75.3 MB (75345562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f87483a63057b23d2d2122d4fdabdc965bb7e650da968fcd786c61f0994d563c`  
		Last Modified: Tue, 03 Jun 2025 18:51:17 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1f0c676bba1dac857bd4dbe40d2a834f91435df361fbe1c01db71793737606f`  
		Last Modified: Tue, 03 Jun 2025 18:51:18 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:835175b59ed3c3085f86a15190dd8403a6082bd69ca9ddedc305487b79f13143
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4982582 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de01d4fd7717e1f3e0a028658cf59c50c63cb81268d8eaca11a44c354da4da2d`

```dockerfile
```

-	Layers:
	-	`sha256:fadd53e5ce41f5f056b8b52be881d2de1fbc101e7a029177dc7de00987770403`  
		Last Modified: Tue, 03 Jun 2025 21:37:38 GMT  
		Size: 5.0 MB (4966656 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:768d96dc73e07d193c0e77bf3d4e97053fcf547624f27aacf6583a78fdbf0c16`  
		Last Modified: Tue, 03 Jun 2025 21:37:39 GMT  
		Size: 15.9 KB (15926 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-bookworm-slim` - linux; s390x

```console
$ docker pull clojure@sha256:38e192bf84f91dd198a36b60525ef083ea41efbc852db62f77bb610106b7dcea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.9 MB (229891472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:402295e285350e4fa9a6fb67479dbf8fee57c6dbbf252bf66bd6273ffb76bc28`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1747699200'
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
	-	`sha256:fb6e196ef379785f6b759a20e90d74fe0566b240771695f724c27a44aa6cd3ce`  
		Last Modified: Tue, 03 Jun 2025 13:31:54 GMT  
		Size: 26.9 MB (26882808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ad34fa5b937772a939247553d5da11fa707ffc251f370c152ab8bf4d478cc3f`  
		Last Modified: Tue, 03 Jun 2025 06:13:21 GMT  
		Size: 134.7 MB (134673554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33c4419f68bff1b27b7cb67ee73b238c394cf03bddeeb34eb893acbc04736e8e`  
		Last Modified: Tue, 03 Jun 2025 18:33:11 GMT  
		Size: 68.3 MB (68334069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a90a773b44a6fbd967ddeffd21630379a33d5f5aa33f2b21d502f753d050b7ce`  
		Last Modified: Tue, 03 Jun 2025 18:32:49 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4946f21b5ff1d56fa80ce47e6588218eb342db7e3def35a35b740a988f91cc0a`  
		Last Modified: Tue, 03 Jun 2025 18:32:49 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:42fa9fa3ae7abd386eaa75c737038a986fcfc21f5f47f7fc51b487a954d9a80f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4971590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:949421544a0457e54067237711b57ac4505c6bcd5c42b63f884baf7a7fefeef2`

```dockerfile
```

-	Layers:
	-	`sha256:868f7cbe8a2d277b25ca3852d6a4910ef3532b214e8be7e111379889760992cc`  
		Last Modified: Tue, 03 Jun 2025 21:37:44 GMT  
		Size: 5.0 MB (4955711 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:51d58268a0d406b7c42b2e75279f592dcbe2e8751263811b8b296058bdc6722e`  
		Last Modified: Tue, 03 Jun 2025 21:37:44 GMT  
		Size: 15.9 KB (15879 bytes)  
		MIME: application/vnd.in-toto+json
