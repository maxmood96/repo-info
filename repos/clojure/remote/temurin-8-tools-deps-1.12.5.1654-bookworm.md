## `clojure:temurin-8-tools-deps-1.12.5.1654-bookworm`

```console
$ docker pull clojure@sha256:c9e0703530a7ce559e4cb95a0f493c99f121d50d2edd7d75dca6852366e71618
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-1.12.5.1654-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:45a9193bfc9d3f24d66ebb7799f9b08de639b0047ba3506cb4f31c68eb703144
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.8 MB (181826306 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d20daa01b9959804e2bb6673879638cd3416db73bfdb41d78d465c45702a86e`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 01:15:24 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Jun 2026 01:15:24 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 11 Jun 2026 01:15:24 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jun 2026 01:15:24 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Thu, 11 Jun 2026 01:15:24 GMT
WORKDIR /tmp
# Thu, 11 Jun 2026 01:16:27 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 11 Jun 2026 01:16:27 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 11 Jun 2026 01:16:27 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:01cedcff86f879d042805360ecba268802bec3d8201484ff3ec54f4250a2d3b7`  
		Last Modified: Wed, 10 Jun 2026 23:39:39 GMT  
		Size: 48.5 MB (48502042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:057b038e1a618bf416ac56320d08631c6361bca17d111ee68f23756b0466de56`  
		Last Modified: Thu, 11 Jun 2026 01:15:58 GMT  
		Size: 55.2 MB (55198715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8b37c452eafe6715cbf4c387b542ca7bacb5d90e08561e5a8b9a3caab62fe86`  
		Last Modified: Thu, 11 Jun 2026 01:16:45 GMT  
		Size: 78.1 MB (78124905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6d25a22a60b7f0d4723fc5e74fd538ca79f42268d2ca80716fc594df7e1758e`  
		Last Modified: Thu, 11 Jun 2026 01:16:43 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.5.1654-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:2deed72c5bc0c02223489ae5c38e9d24c3683052643baffdfd5795fac723c895
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7509888 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e924e19d93cffe29bb00d41930530b630bbcc9df399218758dcb4162b636c8f`

```dockerfile
```

-	Layers:
	-	`sha256:70b660a8907d12027bcbe4c97aa1faa7460b9e60f52d2c675107c4caee1f2d6c`  
		Last Modified: Thu, 11 Jun 2026 01:16:43 GMT  
		Size: 7.5 MB (7496494 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:28299c643c85c7b4d23f215b95f743f335646373f0965f17d345c9942b437ad4`  
		Last Modified: Thu, 11 Jun 2026 01:16:42 GMT  
		Size: 13.4 KB (13394 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-1.12.5.1654-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:6e58a684e0221eff4b6cc5e05cc42d8dcef2a38d8a95e93dcfb98220c3002abe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.8 MB (180792248 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4c1762d7766c017e47199af470b299b0c5b7cd53cfc0f70019980c4f03d09ae`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 01:20:19 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Jun 2026 01:20:19 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 11 Jun 2026 01:20:19 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jun 2026 01:20:19 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Thu, 11 Jun 2026 01:20:19 GMT
WORKDIR /tmp
# Thu, 11 Jun 2026 01:20:33 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 11 Jun 2026 01:20:33 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 11 Jun 2026 01:20:33 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:c847f328095fb083f4a22895b90fe4226efa6458ac57362b64b6e5d99da9e4a3`  
		Last Modified: Wed, 10 Jun 2026 23:39:28 GMT  
		Size: 48.4 MB (48389016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f26e1eae44f5ddb089438f20287cd70de0953dad2bb913a6593a65e868c37cdc`  
		Last Modified: Thu, 11 Jun 2026 01:20:52 GMT  
		Size: 54.3 MB (54272936 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3bce69fb833d5ba981ce05a80bf9a97e5ac5c99d2668e50f023c923952bc4e9`  
		Last Modified: Thu, 11 Jun 2026 01:20:53 GMT  
		Size: 78.1 MB (78129653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b205ad0ada1f7d871b9722fd5a2d734f2c8341723b030f3c09ec199b75cb20eb`  
		Last Modified: Thu, 11 Jun 2026 01:20:50 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.5.1654-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:2a302a1b7d38df515206db8f1d4ab8b29a2725a81c943b5253aacffc3fcc2dfb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7517422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:711079382af2685c4cd0e8295d0a254ca236d0885e0ee870d5028fee09843902`

```dockerfile
```

-	Layers:
	-	`sha256:5f4cd6ab65602e637eb460edd9c5e2bcb93f72646298d7284ce65a795193926f`  
		Last Modified: Thu, 11 Jun 2026 01:20:51 GMT  
		Size: 7.5 MB (7502957 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5e37d6eae79d5728b562bf287247b6cfaf8e738e772581e8824a5bab2090631d`  
		Last Modified: Thu, 11 Jun 2026 01:20:50 GMT  
		Size: 14.5 KB (14465 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-1.12.5.1654-bookworm` - linux; ppc64le

```console
$ docker pull clojure@sha256:55667d078687b7e7cda7b9606c72ad7b4aed897e8d7079a6f69118133e97b956
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **189.0 MB (188975164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6c66a14518a8aaf851fbea48df4b82317c6753cfed7090fdb3125aa6e9a379c`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 09:15:04 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Jun 2026 09:15:04 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 11 Jun 2026 09:15:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jun 2026 09:15:04 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Thu, 11 Jun 2026 09:15:04 GMT
WORKDIR /tmp
# Thu, 11 Jun 2026 09:19:21 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 11 Jun 2026 09:19:21 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 11 Jun 2026 09:19:21 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:88b94a58fac236a778527a3293ccd0ff4d309bff0bf314017ea5af603908fa2e`  
		Last Modified: Thu, 11 Jun 2026 00:21:34 GMT  
		Size: 52.3 MB (52346670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e9782e699ff95e8ba0baef1eb1b0a8eef351ff0363848398eeeccc46af5f13a`  
		Last Modified: Thu, 11 Jun 2026 09:16:11 GMT  
		Size: 52.7 MB (52669122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b95cf93592a533a2eddb9b91d935f081a9102f50481decd4a4174204b0ff0094`  
		Last Modified: Thu, 11 Jun 2026 09:19:56 GMT  
		Size: 84.0 MB (83958728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4849faf94cb0505b0bc54009e54581b0f0d813d2402635f834fb858843b3937d`  
		Last Modified: Thu, 11 Jun 2026 09:19:54 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.5.1654-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:56a34640492a96f381b4131440fef98a5ed88c799cfae9a6dac9a7485ea33377
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7516701 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3a4ecdb54f4863c8bc0ca4e8feaa83c00427e97cebe785cd683f9970d90038e`

```dockerfile
```

-	Layers:
	-	`sha256:2304f8c6612eb44dcefadd0a947d318ca8c267a8b7bb1a047519f7827ca3343f`  
		Last Modified: Thu, 11 Jun 2026 09:19:54 GMT  
		Size: 7.5 MB (7502305 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:48ec8453f9efcff4a4df143d53800cf37dccc91f7eedbeb0d6d2abac7dc10957`  
		Last Modified: Thu, 11 Jun 2026 09:19:53 GMT  
		Size: 14.4 KB (14396 bytes)  
		MIME: application/vnd.in-toto+json
