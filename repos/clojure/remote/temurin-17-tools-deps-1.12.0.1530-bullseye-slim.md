## `clojure:temurin-17-tools-deps-1.12.0.1530-bullseye-slim`

```console
$ docker pull clojure@sha256:fb44ee19b861d896b01904a62553687c66dca43fde6aa2ef96304b33f6f8f516
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-tools-deps-1.12.0.1530-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:14686bfb41dbef14ea903478544760858f0c04a0be84e56cda2315f6da29d690
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.9 MB (233883511 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:575bba59bf2a9b7a593121aa3f4175a6ae2724d5b45daec5333ad25f83526bf1`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1745798400'
# Mon, 28 Apr 2025 17:24:54 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 28 Apr 2025 17:24:54 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 28 Apr 2025 17:24:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 28 Apr 2025 17:24:54 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Mon, 28 Apr 2025 17:24:54 GMT
WORKDIR /tmp
# Mon, 28 Apr 2025 17:24:54 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 28 Apr 2025 17:24:54 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 28 Apr 2025 17:24:54 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 28 Apr 2025 17:24:54 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 28 Apr 2025 17:24:54 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:c8e1eb8ab3b017bd9e33ddec83ebdd8292c542bbd14a8d5a6cfa2edc3ad3b8eb`  
		Last Modified: Thu, 08 May 2025 17:04:40 GMT  
		Size: 30.3 MB (30254604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ffeabfb2d9fc4a0c541374f73caf24c5230cd0fc3931142e91473df8f662723`  
		Last Modified: Mon, 05 May 2025 17:07:36 GMT  
		Size: 144.6 MB (144635029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f08c06b9df357b383af104be063e20245df5e89451c246552ffd32f390b6e3c7`  
		Last Modified: Mon, 05 May 2025 17:07:35 GMT  
		Size: 59.0 MB (58992840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0f22f3da9895ce82dd1ca46b6928edb34c2194d2528800e368f838423e26b6f`  
		Last Modified: Mon, 05 May 2025 17:07:34 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a9d29b4ffff5f1cba3c911fba8e40639361f481b409cb0310f418ec2ab05f09`  
		Last Modified: Mon, 05 May 2025 17:07:34 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.0.1530-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:b600419dbddc5e516065b03310e9f241a3db9d8d662fdae13c286f39210906e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5134946 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc76b8b541c72569515b96e94b63fe9d76796228942701de04bc95fff0213c5d`

```dockerfile
```

-	Layers:
	-	`sha256:cc899bba178f73ee0db07e9e793fed60f2286a8225b6e7f5cf6deddaa4f969f3`  
		Last Modified: Mon, 05 May 2025 17:07:34 GMT  
		Size: 5.1 MB (5119067 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f0b0b2f08f2bc880f438f8207eaa5a05bf57d514f5303c586493237bce56af08`  
		Last Modified: Mon, 05 May 2025 17:07:34 GMT  
		Size: 15.9 KB (15879 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.0.1530-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:3abdd7e7ef084cef93e4f2f48440b2e25feab6484c755c8a161dd1de7ca1aba2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.4 MB (231385807 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7312dafc6531de0d96ef3028cf9859ab0e4073d30c0213a8fc2db549265bc94d`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1745798400'
# Mon, 28 Apr 2025 17:24:54 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 28 Apr 2025 17:24:54 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 28 Apr 2025 17:24:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 28 Apr 2025 17:24:54 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Mon, 28 Apr 2025 17:24:54 GMT
WORKDIR /tmp
# Mon, 28 Apr 2025 17:24:54 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 28 Apr 2025 17:24:54 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 28 Apr 2025 17:24:54 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 28 Apr 2025 17:24:54 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 28 Apr 2025 17:24:54 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:5d3a81360c5bb9281a4f735a1468429a1898f1a4fc24a2581dde4cf28ace4488`  
		Last Modified: Thu, 08 May 2025 17:04:53 GMT  
		Size: 28.7 MB (28744645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:089ae675387ee815f1cf9a4635844bb9773f6f4159669c6ceed3939975ea5d1a`  
		Last Modified: Thu, 08 May 2025 17:45:38 GMT  
		Size: 143.5 MB (143512640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71e49d5bf8561b111ab4b32bcf1f994116add29b8ebfe31d40008de774ab8d5e`  
		Last Modified: Tue, 06 May 2025 00:39:04 GMT  
		Size: 59.1 MB (59127482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1ad8e135aeb9dfc2d1f9ff84c1c4ed1554ead13e951b3bb4b4e1aafcf8ca35d`  
		Last Modified: Tue, 06 May 2025 00:39:02 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27944530a67621ffe0a2c46389f78e9ffb3b5851803d74a5af960f7015912cff`  
		Last Modified: Tue, 06 May 2025 00:39:02 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.0.1530-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:b2ff5b4e4c3919141eecb131f54459188ab66ba5a7b1ee30694cfaa6a0c6105d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5140795 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdff02a19f2a4a81c16b93dab282872f6600a55860be678e86aa884f154aca50`

```dockerfile
```

-	Layers:
	-	`sha256:7f84c9ff1b7700d267cd83ecac33a814dbf8887b845564c0bf377c449f5dbfed`  
		Last Modified: Tue, 06 May 2025 00:39:03 GMT  
		Size: 5.1 MB (5124799 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b3b7319c31b3e83bb327f16103eda4f4b7a1a1a37f3776241603f653c05b96f0`  
		Last Modified: Tue, 06 May 2025 00:39:02 GMT  
		Size: 16.0 KB (15996 bytes)  
		MIME: application/vnd.in-toto+json
