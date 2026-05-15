## `clojure:temurin-11-tools-deps-1.12.5.1638-bullseye-slim`

```console
$ docker pull clojure@sha256:14e73570ee61bcdf7818469c97437ee72516f87c2d59adacf508317ac2113940
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-tools-deps-1.12.5.1638-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:a0b9bdb440fdf1c7d84efafb3808b7c73dbdcfbbdfa0f2cacf0164b1f26d8cba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.4 MB (235359912 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc3ae3032c158c7e074c03456bb513c392214e3be2d55dbd964c3a289e9aafa4`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1777939200'
# Thu, 14 May 2026 23:34:25 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 14 May 2026 23:34:25 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 14 May 2026 23:34:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 14 May 2026 23:34:25 GMT
ENV CLOJURE_VERSION=1.12.5.1638
# Thu, 14 May 2026 23:34:25 GMT
WORKDIR /tmp
# Thu, 14 May 2026 23:34:38 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "bccfca8c437514786f0827a11195b89b833357b2a668091f4321b451b2e36df5 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 14 May 2026 23:34:38 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 14 May 2026 23:34:38 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:77e30ef52aeb52d8466baf0f50b54ed2fc0b421f44c49e5bf93682b27110f4d3`  
		Last Modified: Fri, 08 May 2026 18:22:59 GMT  
		Size: 30.3 MB (30257958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:582837acbb13865dc0d279b2835e5c9df38df5eb0048d170a5ff0b6e51ce04a0`  
		Last Modified: Thu, 14 May 2026 23:34:58 GMT  
		Size: 145.9 MB (145886219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8bbe07c75a01c4daf6cb058a0f4d2800afcd2927b6408e5228040d500dc125b`  
		Last Modified: Thu, 14 May 2026 23:34:56 GMT  
		Size: 59.2 MB (59215086 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59573d002c88ddbd896299a047d4d389090e03dd4fc27684812a4bde67576226`  
		Last Modified: Thu, 14 May 2026 23:34:53 GMT  
		Size: 617.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.5.1638-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:ee93b4601a899d648da5751aa7826d0a050682e34579be7eae671f4db90ed5c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5354615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3232959c84e13a21f02135d19b135d07ef11ecba733253f9f47f0b5aa98f0d80`

```dockerfile
```

-	Layers:
	-	`sha256:da58726eb77816fda9dc73920ce640c426796e35ff4d3840e0a6fffbab6c24a9`  
		Last Modified: Thu, 14 May 2026 23:34:54 GMT  
		Size: 5.3 MB (5340194 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:137b200d786371df8fee02308374845490ee0845fb119c7f42f554a937de22b6`  
		Last Modified: Thu, 14 May 2026 23:34:53 GMT  
		Size: 14.4 KB (14421 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-1.12.5.1638-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:d3b9f78644feb0410729a1f4bed0d8dbffa9d3395cf80dc979708b298608e56e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.7 MB (230683750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27fde4f9e244384253207a6a450b0cce9f239d3bf9a9bd1b53b781e9044d7111`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1777939200'
# Thu, 14 May 2026 23:34:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 14 May 2026 23:34:18 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 14 May 2026 23:34:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 14 May 2026 23:34:18 GMT
ENV CLOJURE_VERSION=1.12.5.1638
# Thu, 14 May 2026 23:34:18 GMT
WORKDIR /tmp
# Thu, 14 May 2026 23:34:31 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "bccfca8c437514786f0827a11195b89b833357b2a668091f4321b451b2e36df5 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 14 May 2026 23:34:31 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 14 May 2026 23:34:31 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:ab0f13d792ff9100407906fb422a0b62a8b437abde4c245e03f0366814be9aae`  
		Last Modified: Fri, 08 May 2026 18:25:06 GMT  
		Size: 28.7 MB (28742591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba8bf2c09bbad533bbc490d112b59439f90006ce0c83a7b1e435668fc06a5fb3`  
		Last Modified: Thu, 14 May 2026 23:34:52 GMT  
		Size: 142.6 MB (142582199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b02654f072fa274f24fcbe5e4a8db32eca38260e6ced3f31292d9f66c30390ec`  
		Last Modified: Thu, 14 May 2026 23:34:51 GMT  
		Size: 59.4 MB (59358311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ffe951fbad7f6a0cbab220daa5212d11fc22b5729aed1ad00184ca1ca7e63c3`  
		Last Modified: Thu, 14 May 2026 23:34:48 GMT  
		Size: 617.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.5.1638-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:df28868acfe9a07c7b4d28ce4139fba589a4a296e522bc8c9852d900a5546957
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5361083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24ad81b7b7b7d84f055b363c97ac3a5e5d307aaf82819aee3b5ee356c6797d15`

```dockerfile
```

-	Layers:
	-	`sha256:3f41cba152c5fffdf881a9acbf29328600cc1f6b446aaed9b6bce6d30d839a44`  
		Last Modified: Thu, 14 May 2026 23:34:49 GMT  
		Size: 5.3 MB (5346544 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3e0855b1da8c49c9ef3ea9f9b9a31780310013085b92facd1c32f68b354eed9a`  
		Last Modified: Thu, 14 May 2026 23:34:48 GMT  
		Size: 14.5 KB (14539 bytes)  
		MIME: application/vnd.in-toto+json
