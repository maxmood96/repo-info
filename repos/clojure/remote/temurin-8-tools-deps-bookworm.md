## `clojure:temurin-8-tools-deps-bookworm`

```console
$ docker pull clojure@sha256:70de005bc90501df292a5d3d6784ac505bd312ac116a000d744dc885fc9f89b5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:cf8933f362fe4c696241ef52bb3cc15c3b953c8ca60774057bd1f10ff19640d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.4 MB (184361717 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfd9ad626aacffdf45314e4d712ea32e049f81653cb1afc14889283ca47f29c7`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1768176000'
# Fri, 16 Jan 2026 01:43:40 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Jan 2026 01:43:40 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 16 Jan 2026 01:43:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jan 2026 01:43:40 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Fri, 16 Jan 2026 01:43:40 GMT
WORKDIR /tmp
# Fri, 16 Jan 2026 01:43:55 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 16 Jan 2026 01:43:55 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 16 Jan 2026 01:43:55 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:c1be109a62df95316ceac87ea501079f32e17f36b636865a860841b7db06100c`  
		Last Modified: Tue, 13 Jan 2026 00:41:40 GMT  
		Size: 48.5 MB (48481622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3290f95383b389f6f96fec1f15b598ff1bb52477f3da21e7e1f6649b9b2db41c`  
		Last Modified: Fri, 16 Jan 2026 01:44:40 GMT  
		Size: 54.7 MB (54733367 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3097775fb9485c3df3df8f4184bd50d87a7a59eec2d26028790a0051302458d2`  
		Last Modified: Fri, 16 Jan 2026 01:44:14 GMT  
		Size: 81.1 MB (81146083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b701e9633e538f91e2ca2fb4a8f794003c61dd45b026b1e9766d752ef45869b2`  
		Last Modified: Fri, 16 Jan 2026 01:44:11 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:7b23e0af1aa2a67294cc67055008e168c31865d2abf9a23bdb09809f32648e06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7511337 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a26e171d6d3d1809697581d7785ba54725519d3ed056c53e23a87e57541a766`

```dockerfile
```

-	Layers:
	-	`sha256:80e557a6e8a40468645842de3a48349cf21278d1651235b59e1877f022a80cdd`  
		Last Modified: Fri, 16 Jan 2026 04:52:04 GMT  
		Size: 7.5 MB (7497143 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fa5523ec70824f0c5c5402b50143faf5db4f4ac9cde74da1e68c39b3c2c52528`  
		Last Modified: Fri, 16 Jan 2026 01:44:11 GMT  
		Size: 14.2 KB (14194 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:72ebdf7433e89ec1bae58f26e43b6b31c5ee3441929b4329fb117d835e223e10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.3 MB (183320818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec9b9949c7d7f98c6212a3b34b090b9e5923bef4217598908bf9d15956ff6aa7`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1768176000'
# Fri, 16 Jan 2026 01:42:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Jan 2026 01:42:46 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 16 Jan 2026 01:42:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jan 2026 01:42:46 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Fri, 16 Jan 2026 01:42:46 GMT
WORKDIR /tmp
# Fri, 16 Jan 2026 01:47:26 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 16 Jan 2026 01:47:27 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 16 Jan 2026 01:47:27 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:1029f5ddc0d24726f1cefbb8def7a88f8ec819a1fdc4c05ce523011b4b73c72d`  
		Last Modified: Tue, 13 Jan 2026 00:41:14 GMT  
		Size: 48.4 MB (48366072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c79a06fd9c520fe2ee5fc0d30a9341d9c16bbaeaa191b97557c075786652c69`  
		Last Modified: Fri, 16 Jan 2026 01:46:43 GMT  
		Size: 53.8 MB (53814998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c96bea1e18618aca1e30558581bcd6e71e37b310246bd8cfc59748af57e65d47`  
		Last Modified: Fri, 16 Jan 2026 01:47:46 GMT  
		Size: 81.1 MB (81139102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3973324e00e66942afe32af70e42cb85df0309589860f5e1509421b540b071f2`  
		Last Modified: Fri, 16 Jan 2026 01:47:53 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:a7a86a5dce4f4588ceeed08ad2f4f71f3e5cbf1595a42038b51d65cadaf64afc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7517116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a56fba157119d57317b0befb2153a465ad13dcf118b62795891d424a8f4eabe1`

```dockerfile
```

-	Layers:
	-	`sha256:632a0b215a490da80992976be98386554be0db14537a21c1d25a27e70f62d164`  
		Last Modified: Fri, 16 Jan 2026 04:52:11 GMT  
		Size: 7.5 MB (7503604 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:67c4eed7ebb940c6c9b261665cbf10b79d22abb4ce2e83cf24c2d16ce2cad9fa`  
		Last Modified: Fri, 16 Jan 2026 04:52:12 GMT  
		Size: 13.5 KB (13512 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-bookworm` - linux; ppc64le

```console
$ docker pull clojure@sha256:f1d449f3da4b36b6583734bbb106bb5b9fc4d07759279dfb489be68e4a530968
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.5 MB (191489724 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4446dda3ee5c272ee128ea8f6f4ae12bc5382309bcd96afb702a211a7cb3bd1f`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1768176000'
# Fri, 16 Jan 2026 02:45:24 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Jan 2026 02:45:24 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 16 Jan 2026 02:45:24 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jan 2026 02:45:24 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Fri, 16 Jan 2026 02:45:25 GMT
WORKDIR /tmp
# Fri, 16 Jan 2026 02:51:35 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 16 Jan 2026 02:51:35 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 16 Jan 2026 02:51:35 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:7fcf9f2b462d6af06c3ad2420b999e6b092984c4723ebac480c428a5d837d3b7`  
		Last Modified: Tue, 13 Jan 2026 00:40:39 GMT  
		Size: 52.3 MB (52327376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eacc98e18f5511676874243a42251586a4bb8213c4780fdafb56a8f17cf4cc5a`  
		Last Modified: Fri, 16 Jan 2026 02:47:01 GMT  
		Size: 52.2 MB (52175125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aeee78c4588d35243a1267e6b9ebc2fbfb29cbafdf9627458b07718324d719b0`  
		Last Modified: Fri, 16 Jan 2026 02:52:34 GMT  
		Size: 87.0 MB (86986579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:011fea76abc45777067e4f5b8f8455ffd92362e912c159e79a53ffb3c72cf697`  
		Last Modified: Fri, 16 Jan 2026 02:52:24 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:ffa54683ea84fa1839dda77833722859f9ca5273904b838c569895d70acd6683
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7517194 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55c3c61d31c42c35826c03485771a142e191958b39069b37e54ad000fda33755`

```dockerfile
```

-	Layers:
	-	`sha256:0cb1bca03835db3f21deef1961ef7f04d279f5a93aedd0c52b9a09f435d77b46`  
		Last Modified: Fri, 16 Jan 2026 02:52:15 GMT  
		Size: 7.5 MB (7502952 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6fd94e704f3b383da12c5182c6c2a992c6d375e628f6c0653de60a4bcaddf377`  
		Last Modified: Fri, 16 Jan 2026 04:52:19 GMT  
		Size: 14.2 KB (14242 bytes)  
		MIME: application/vnd.in-toto+json
