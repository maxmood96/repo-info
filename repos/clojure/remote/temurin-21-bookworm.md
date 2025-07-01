## `clojure:temurin-21-bookworm`

```console
$ docker pull clojure@sha256:5e12d452bc737f92f8c758a50ab87712487c62bd49c2fd565c774cb382cf7f26
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

### `clojure:temurin-21-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:82b133bdea86dedc131e3709105ea22e98ca54e987cc43f301fced91c0b914ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.1 MB (287122732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b7bf3ec0f50b3457a0a96825f62a8a321aec05d895c28498ea091a3bb955de7`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1751241600'
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
	-	`sha256:c1995213564325caf7e52ecd95fe4435c70b03eb94c674ac15706733986b86e0`  
		Last Modified: Tue, 01 Jul 2025 01:14:44 GMT  
		Size: 48.5 MB (48494284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24e78cd354fe4b3fed7295da6ea1671d0fa79052733bf807863822f394cd598a`  
		Last Modified: Tue, 01 Jul 2025 06:52:48 GMT  
		Size: 157.6 MB (157634503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bc2f0a825070aa7c8ab3971f59e2b4f100714ad969ee929b04a5f7f8f10ec4b`  
		Last Modified: Tue, 01 Jul 2025 06:52:44 GMT  
		Size: 81.0 MB (80992905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35c2df9bde9d640dd6555eca2e8479831387c343ba17d115ed516840ff25b995`  
		Last Modified: Tue, 01 Jul 2025 03:45:16 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2631f633b64eed753b565bfc70f5aeebdd05d429a69e594e662131b13cda04b`  
		Last Modified: Tue, 01 Jul 2025 03:45:19 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:dedc6ed49f347c1a39ede5ea20ef4de8f8b93089c8ecefa9e0dbb8529ab98341
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7391191 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6556488f2e126052af04b78753bd90ea3d3e6c7f76e3963db7ac026c1729b4b`

```dockerfile
```

-	Layers:
	-	`sha256:762584053f7524b62cd92940590dd750293c57fce99ce1b750e1edbd480c72e1`  
		Last Modified: Tue, 01 Jul 2025 06:38:40 GMT  
		Size: 7.4 MB (7373370 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f6f006205f22851cd9bf62c88311b704e8bc861f57199a6ec3b2a23d3792b9a2`  
		Last Modified: Tue, 01 Jul 2025 06:38:41 GMT  
		Size: 17.8 KB (17821 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:3949dc92c27d15ee0d29aecd0288cf46258ccbe1e52afd4ca4f3e41e1014a6a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.1 MB (285117012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9e9ddc430ee3abb832d0810ce6a748daa6e764da426a450fe822e3cd283faac`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1749513600'
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
	-	`sha256:8fbf1dd6492cb885c9004e9e7ecb0880a823cd140e63f4b13dfc1bc4d0d3e37b`  
		Last Modified: Tue, 10 Jun 2025 23:26:40 GMT  
		Size: 48.3 MB (48338852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd2c862dd63a0f06c6065a1f9eebb4c4c8659cf987595881d27397c18e9bfa45`  
		Last Modified: Wed, 11 Jun 2025 10:01:03 GMT  
		Size: 155.9 MB (155928834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaf79607a6c72b41cd02f016b0072fbb43652314475655aaef94ab35feaf2ea7`  
		Last Modified: Wed, 11 Jun 2025 10:01:13 GMT  
		Size: 80.8 MB (80848286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65f8affce2492591b9f679baf0040545186501ba1bf6d5553766c0fb22e10c3e`  
		Last Modified: Wed, 11 Jun 2025 08:38:06 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e5e85bfbf785f086e58debb89435789db853baccc105dde551449fc19d5082d`  
		Last Modified: Wed, 11 Jun 2025 08:38:09 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:5e6f6a66b69d614e3de9b7a2ba7b820f774fdfebf57e93de6a72fb83d94c3471
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7395860 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8ff1d45df3e14fd18cca533935ef928cee510f18e9ca07d2749d78da46118b2`

```dockerfile
```

-	Layers:
	-	`sha256:8ade275353c4e98f242072cbbfb44e08232067dd8c84ace42f0c329e73ee34fc`  
		Last Modified: Wed, 11 Jun 2025 09:39:17 GMT  
		Size: 7.4 MB (7377849 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f25c323af4f9d64bf5a3ea60d53489c533f9ecbbbc907eb70c582d42d8d7d203`  
		Last Modified: Wed, 11 Jun 2025 09:39:17 GMT  
		Size: 18.0 KB (18011 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-bookworm` - linux; ppc64le

```console
$ docker pull clojure@sha256:385da27bf44357d59831bb26077d6afca23ed47c6c0eca452f950424ecaaea63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.0 MB (296962910 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d568cc11932336b7862bae35ab5ed0c890d8a693d4adc5fd593b373a7685a37d`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1751241600'
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
	-	`sha256:2819217d87219cbf8b5ec7dfbc47c9a16195c7992a9fbe92da8723c42180b19b`  
		Last Modified: Tue, 01 Jul 2025 01:15:05 GMT  
		Size: 52.3 MB (52337243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8eb00989eb2ecd00cd9ea5051b21c8185732aa39815a0ceb06473d7cf6668084`  
		Last Modified: Tue, 01 Jul 2025 08:12:49 GMT  
		Size: 157.8 MB (157804868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bfdd9675151df8f7201d1511a9351309b60faa1e8d916291ed0d5f2979d816e`  
		Last Modified: Tue, 01 Jul 2025 09:03:07 GMT  
		Size: 86.8 MB (86819756 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ffe58fbb068e44d14db9cd0dc093e8a4749a4938a52b99c1449784c7ef7122d`  
		Last Modified: Tue, 01 Jul 2025 09:02:59 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1767c04bc56a76b4736b5a742d1274ec1881e0d7448df9f4aee39116cb1eb10e`  
		Last Modified: Tue, 01 Jul 2025 09:02:58 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:7439b919a0ff322981a10d9b2a598d2fc61a777cfe1f8fbda2691ea77097894f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7396514 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9d5aad83a691f1691192feff664ba9abb948ac63606b7234c84b79a7a986dda`

```dockerfile
```

-	Layers:
	-	`sha256:e855903064515039d57bf08e1e29c2b0942035bcece434373c3a51d3d862dc68`  
		Last Modified: Tue, 01 Jul 2025 09:39:46 GMT  
		Size: 7.4 MB (7378610 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0a81e9ff65f83b4e72dd49e8428a651b47c924e2e1f1757860ce5843530ca320`  
		Last Modified: Tue, 01 Jul 2025 09:39:47 GMT  
		Size: 17.9 KB (17904 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-bookworm` - linux; s390x

```console
$ docker pull clojure@sha256:ac7b21d6bf98b2c1176df4d580471384b793211b97f61bb3e36def21dbda84f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **273.9 MB (273860830 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4001819ce194a5a9cefc1b670af996aadfac3e79cffabd8a7f263981e1efaa86`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1751241600'
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
	-	`sha256:f5e945529523ccd9610b7c0253cda59a29c297f0a697f3c402695e1c6ecf5e6c`  
		Last Modified: Tue, 01 Jul 2025 01:15:47 GMT  
		Size: 47.1 MB (47149287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b56a47b9ba84bc64ca6ce5c5309a2eafe1d1c6565b113770245512f1bfe041ca`  
		Last Modified: Tue, 01 Jul 2025 08:00:49 GMT  
		Size: 146.9 MB (146910995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f6d6537d8c279e3b7ae26098509441b14ac81762abac0e0503a92e2b2aa9d9e`  
		Last Modified: Tue, 01 Jul 2025 08:21:01 GMT  
		Size: 79.8 MB (79799510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d16c54e4566435b1980b702be5e1808fab2a3d3cc30edddb1a9541bb135ce22`  
		Last Modified: Tue, 01 Jul 2025 08:22:15 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a96bd86d929de3365d8c19b5e664f8e7ced4813ba3dc27e1146035ee32ccaaa`  
		Last Modified: Tue, 01 Jul 2025 08:22:17 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:7c9e93451a421856751c751632b116e265b1fb78292e4897c19786e2ade3d885
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7382510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53fe4a8b63ab1bc800ec28a340e64aef2e88bd9ddbbb9a9fa2b1a006e051671d`

```dockerfile
```

-	Layers:
	-	`sha256:ab62f1caaf0333351e65fcbf569bc91ba777aeda98b27754bc2f14a832ba3c88`  
		Last Modified: Tue, 01 Jul 2025 09:39:51 GMT  
		Size: 7.4 MB (7364689 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:12ffadbffa1551def48af560466e59cd4cae9c6f5ad8b284c196ef833a9aeb2e`  
		Last Modified: Tue, 01 Jul 2025 09:39:52 GMT  
		Size: 17.8 KB (17821 bytes)  
		MIME: application/vnd.in-toto+json
