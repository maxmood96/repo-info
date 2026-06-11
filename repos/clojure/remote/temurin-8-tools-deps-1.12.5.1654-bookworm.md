## `clojure:temurin-8-tools-deps-1.12.5.1654-bookworm`

```console
$ docker pull clojure@sha256:a0e4e46b14d9b1fbdadcb001f82256a3f6aea5242f1da84e2e654bd513ff8acd
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
$ docker pull clojure@sha256:8bc9888055e31895460f60ca958f16f9b9025617411de81f3499946702911e52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **189.0 MB (188969443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19a2a7ee09c1ac8d0164bffc506db33a6f8faaa4267e080553f205031bb3abea`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1779062400'
# Thu, 04 Jun 2026 17:40:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 Jun 2026 17:40:22 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 04 Jun 2026 17:40:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Jun 2026 17:40:22 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Thu, 04 Jun 2026 17:40:22 GMT
WORKDIR /tmp
# Thu, 04 Jun 2026 17:41:08 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 04 Jun 2026 17:41:08 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 04 Jun 2026 17:41:08 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:b3943e183051423c3dc79fa53ad6d50fff9621945bbfc636eec039b14ead2b66`  
		Last Modified: Tue, 19 May 2026 22:35:10 GMT  
		Size: 52.3 MB (52340199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9545e2d4ebda8e55ef145d34e6940ac7e7ccc363d399c876eb386ef6e83d1ef7`  
		Last Modified: Thu, 04 Jun 2026 17:41:54 GMT  
		Size: 52.7 MB (52669123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34df4fe7cff9f4bb8570ba9add428323c9bbcf3cb37cac931fb0b0c031895c15`  
		Last Modified: Thu, 04 Jun 2026 17:41:54 GMT  
		Size: 84.0 MB (83959473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6294bebc27a3bcad8da12343b8d0112d92a4c50118efb0e157138b4bc4a970e7`  
		Last Modified: Thu, 04 Jun 2026 17:41:51 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.5.1654-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:c8d22af830b74741ea8a63b6a4c648b1264235f014ab2eef5c35e6d0a963f3b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7516683 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:213322bc4d3c85f166e08d2e2ca0f3c0cbc3c89d46bcac66f5000f332e49fb87`

```dockerfile
```

-	Layers:
	-	`sha256:8c8fec3827d04fae1be5dfb06131099bdeb806d176ee481d88d8d25ce095f47e`  
		Last Modified: Thu, 04 Jun 2026 17:41:52 GMT  
		Size: 7.5 MB (7502287 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4d45345172fed7ee781210f98d3c33673eb28083bbbe28bbe380ee9c8cb10e3a`  
		Last Modified: Thu, 04 Jun 2026 17:41:51 GMT  
		Size: 14.4 KB (14396 bytes)  
		MIME: application/vnd.in-toto+json
