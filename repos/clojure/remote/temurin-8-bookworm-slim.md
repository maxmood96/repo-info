## `clojure:temurin-8-bookworm-slim`

```console
$ docker pull clojure@sha256:5c104a3e9450600a7cda2dee1f4d473d1d195c0d5bc46cbafef2de78c538e8ac
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `clojure:temurin-8-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:f981a8d749cb287d0da795d8ef9f77b63fd1f9263a82bcf679fdfea38645af35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.6 MB (152640264 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:880173cc567a95a4450aaf8f0d6fe4e75ccc332b1062fc319fb5de580c339842`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1768176000'
# Wed, 28 Jan 2026 18:03:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 28 Jan 2026 18:03:29 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 28 Jan 2026 18:03:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Jan 2026 18:03:29 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Wed, 28 Jan 2026 18:03:29 GMT
WORKDIR /tmp
# Wed, 28 Jan 2026 18:03:53 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 28 Jan 2026 18:03:53 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 28 Jan 2026 18:03:53 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:c02d17997ce3d2c82e082235ea0b5152d06ee659c4e2fabcf1e0079312f1bcde`  
		Last Modified: Tue, 13 Jan 2026 00:41:44 GMT  
		Size: 28.2 MB (28228572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80db027180f0cfc6607f3b866457d868f8349c47e151c28c8b120cd8fc047fff`  
		Last Modified: Wed, 28 Jan 2026 18:04:12 GMT  
		Size: 54.7 MB (54733313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a0a58090be182a3ad226d770841526948d7c576e12d7713f53eed4bb83d6a4d`  
		Last Modified: Wed, 28 Jan 2026 18:04:13 GMT  
		Size: 69.7 MB (69677735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdf52a835754238f8c8a9370691570cf9f1e4c1432783e104a6c1cf87e96ba2d`  
		Last Modified: Wed, 28 Jan 2026 18:04:10 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:93002cd731060e5a54872dd9bc7316630a1b51833614f28f8fd4e594b4cfb3ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5249258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bab6d968a538a25fb95388c768c8eee33f8a65915f6272792805b86355437b18`

```dockerfile
```

-	Layers:
	-	`sha256:281375f25e5dd54c15a85752c276347650200f1af6e27ca310bda4bc9bee5deb`  
		Last Modified: Wed, 28 Jan 2026 18:04:10 GMT  
		Size: 5.2 MB (5235010 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:52ac16542704c83b8638313401d5a66e3f6709da52b7646610030cc0544fa68b`  
		Last Modified: Wed, 28 Jan 2026 18:04:09 GMT  
		Size: 14.2 KB (14248 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:e94cf4ea39f775a8f82f72e7a393e0e39c5ce15ccbebdd4867ead587c6c23c47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.6 MB (151596364 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f970ca5079d61ebaab34620cc2fe7db21e065e5b4254fde514ea8646cf4b2f04`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1768176000'
# Wed, 28 Jan 2026 18:02:02 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 28 Jan 2026 18:02:02 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 28 Jan 2026 18:02:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Jan 2026 18:02:02 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Wed, 28 Jan 2026 18:02:02 GMT
WORKDIR /tmp
# Wed, 28 Jan 2026 18:02:17 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 28 Jan 2026 18:02:17 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 28 Jan 2026 18:02:17 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:33bdc9671af8942d96d2f78f67aeec06580065dde1272decac3732689ec7c0e8`  
		Last Modified: Tue, 13 Jan 2026 00:42:00 GMT  
		Size: 28.1 MB (28107889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67017648c1e62de972096e17249b6d2119d01e21077166292fe4208678464b43`  
		Last Modified: Wed, 28 Jan 2026 18:02:35 GMT  
		Size: 53.8 MB (53815013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5868e6bca59fe70bef2279af425818a3260c43b99633b6714275bdcaa4f72842`  
		Last Modified: Wed, 28 Jan 2026 18:02:35 GMT  
		Size: 69.7 MB (69672816 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47d1b7bdcf975c57d44b0852b47d82d866de0e6b625a37d6c96ac1e5a3827ba6`  
		Last Modified: Wed, 28 Jan 2026 18:02:33 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:7b231422753d06b52c3f9f9a6570de9adacb625d943768cd06c595eae1e3f5d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5255835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4179aa885de01a93f3adb058bcc6b0ae75665e72f48e261187e091ee41265da0`

```dockerfile
```

-	Layers:
	-	`sha256:b63eb9938dc2612559bde09d1748b804b0eae591def33f93185d37c3339fff48`  
		Last Modified: Wed, 28 Jan 2026 18:02:33 GMT  
		Size: 5.2 MB (5241469 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4a59b20f94fe78e2f0586fe6d064b17cf1e876dd0dd180e041aa932e81a4d79e`  
		Last Modified: Wed, 28 Jan 2026 18:02:33 GMT  
		Size: 14.4 KB (14366 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:d29c06725d8a6fc55df179575efc07911dc035fd0863b7e5de8d36486f4d29d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.8 MB (159758455 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d46f05ab291888a11f6b276543b11c6d4a67b2509812cb059a47a120f20f8bb`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1768176000'
# Wed, 28 Jan 2026 18:02:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 28 Jan 2026 18:02:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 28 Jan 2026 18:02:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Jan 2026 18:02:36 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Wed, 28 Jan 2026 18:02:36 GMT
WORKDIR /tmp
# Wed, 28 Jan 2026 18:03:12 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 28 Jan 2026 18:03:12 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 28 Jan 2026 18:03:12 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:cf92d3bf0add4f20720c3232cd336a7f7f50627989684b748675db0b2f2ce746`  
		Last Modified: Tue, 13 Jan 2026 23:17:03 GMT  
		Size: 32.1 MB (32068709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71d79aadabc182f1ddf05e59cc6c99329b99cf328b2bc4bf79663e6d9bc37d3a`  
		Last Modified: Wed, 28 Jan 2026 18:03:53 GMT  
		Size: 52.2 MB (52175138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a35085582765b057161369577c0b0d16573acda730b4bef5d8056d3e9c9a907`  
		Last Modified: Wed, 28 Jan 2026 18:03:53 GMT  
		Size: 75.5 MB (75513964 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6048325b17cc8e5fa5805bc038807b80d03b9b0f297695905cf1602be182026`  
		Last Modified: Wed, 28 Jan 2026 18:03:50 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:e85d860de6ffe0b69a18de6360b13b479bf37b7a42b86d842dc578ba20c2f568
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5255057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ded8621196e7b8b72473b2c593a7417c01bd4893b80478095b1f052dbf6cdec`

```dockerfile
```

-	Layers:
	-	`sha256:17f0d0bb695fae2d3e728a8e87f8019340f262edf7af1b02ecf44032b5693bda`  
		Last Modified: Wed, 28 Jan 2026 18:03:50 GMT  
		Size: 5.2 MB (5240761 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:00e1bc9ee2ef9a6e6b0eae7b9e07160c48ccadf079eae2160a710a0ac09429ae`  
		Last Modified: Wed, 28 Jan 2026 18:03:50 GMT  
		Size: 14.3 KB (14296 bytes)  
		MIME: application/vnd.in-toto+json
