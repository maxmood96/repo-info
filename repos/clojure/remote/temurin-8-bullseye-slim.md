## `clojure:temurin-8-bullseye-slim`

```console
$ docker pull clojure@sha256:c9d75ad63bd71a0c00ea283d6a5f6d583b99d22c15ee5b87fe381abb7446d1ae
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-8-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:47fa9816611db77d7bcc6e6851dbdfed51f91b951e5367b6108283176d6fa216
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.7 MB (144672723 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8861c625f95d1ccb2fff278937a2eb7b1ce751b9cfd601eb74f5415e0cabcac`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1777939200'
# Thu, 14 May 2026 23:33:45 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 14 May 2026 23:33:45 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 14 May 2026 23:33:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 14 May 2026 23:33:45 GMT
ENV CLOJURE_VERSION=1.12.5.1638
# Thu, 14 May 2026 23:33:45 GMT
WORKDIR /tmp
# Thu, 14 May 2026 23:33:58 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "bccfca8c437514786f0827a11195b89b833357b2a668091f4321b451b2e36df5 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 14 May 2026 23:33:58 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 14 May 2026 23:33:58 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:77e30ef52aeb52d8466baf0f50b54ed2fc0b421f44c49e5bf93682b27110f4d3`  
		Last Modified: Fri, 08 May 2026 18:22:59 GMT  
		Size: 30.3 MB (30257958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0071cd9c5d7f69ecfce0c835df442fea43b36033d275530db1f28130f92e9362`  
		Last Modified: Thu, 14 May 2026 23:34:13 GMT  
		Size: 55.2 MB (55198706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0a944b82bd40d9e4182505d66c2307e137fdc3f7ba368d6d8adac4b3fa9b54f`  
		Last Modified: Thu, 14 May 2026 23:34:13 GMT  
		Size: 59.2 MB (59215414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad01f9e8f8ab4a2326594b80f3c425f8936651ef43c4c798d6f7f36079b82bb0`  
		Last Modified: Thu, 14 May 2026 23:34:11 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:03ad20244ac0ce34ac89d033086460a3f3852d9946ac523ceca3d4c9079569a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5455440 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e47edb35c9cdb9d693b61a812044ea171ff756e6cf6141fc9c99c427c048b77d`

```dockerfile
```

-	Layers:
	-	`sha256:39adbbf6b85b7b8837a8e79f0fe7f72dfc950f8ff06d773bd173cdda7802e570`  
		Last Modified: Thu, 14 May 2026 23:34:11 GMT  
		Size: 5.4 MB (5441038 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4e62a95c186749978dd6a2f9b754d9a3108afd4e0876d44851caa5a1d563020a`  
		Last Modified: Thu, 14 May 2026 23:34:11 GMT  
		Size: 14.4 KB (14402 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:085cda7cbfb9d3ae99152b926d2ad0d1e35667b4f573c1c4f3b41e88b6636df9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.4 MB (142374304 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74015aece93dbd659bc33349591e42e70a49b6b2fc2565b251d422ed64060a2e`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1777939200'
# Thu, 14 May 2026 23:33:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 14 May 2026 23:33:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 14 May 2026 23:33:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 14 May 2026 23:33:36 GMT
ENV CLOJURE_VERSION=1.12.5.1638
# Thu, 14 May 2026 23:33:36 GMT
WORKDIR /tmp
# Thu, 14 May 2026 23:33:49 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "bccfca8c437514786f0827a11195b89b833357b2a668091f4321b451b2e36df5 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 14 May 2026 23:33:49 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 14 May 2026 23:33:49 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:ab0f13d792ff9100407906fb422a0b62a8b437abde4c245e03f0366814be9aae`  
		Last Modified: Fri, 08 May 2026 18:25:06 GMT  
		Size: 28.7 MB (28742591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49e77984e09a76e215aba1eb9f908188d2361978ef53006628647137b6cd4734`  
		Last Modified: Thu, 14 May 2026 23:34:06 GMT  
		Size: 54.3 MB (54272922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:327a16cfacc149670ead39745ef3c0054e645e3f1f98ee697cac57a94ab8947e`  
		Last Modified: Thu, 14 May 2026 23:34:06 GMT  
		Size: 59.4 MB (59358145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ab65bc6492e7584b95cab82dcb79369f0ea602ea9623ff214bacbb313be3d55`  
		Last Modified: Thu, 14 May 2026 23:34:03 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:5ce6627143a03ef81e063fbf71ed9a8470aa92a2399ad03ae2c4cc2fb23498b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5461990 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71b852b855497867bb2e7c8feee9ff0d77e892c0a73ce461090b793ef3e08355`

```dockerfile
```

-	Layers:
	-	`sha256:3196cf2767341e8f8bc11a0149138974977752d2cf830f6c64d40664186db195`  
		Last Modified: Thu, 14 May 2026 23:34:04 GMT  
		Size: 5.4 MB (5447470 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fa544e4fa72efcf51216f496e785679caa7334cb228412aab37365757776c0ba`  
		Last Modified: Thu, 14 May 2026 23:34:03 GMT  
		Size: 14.5 KB (14520 bytes)  
		MIME: application/vnd.in-toto+json
