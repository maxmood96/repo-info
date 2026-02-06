## `clojure:temurin-11-trixie-slim`

```console
$ docker pull clojure@sha256:f6dc9ed6bd16470996ea7063c9804589e6ac721e254ae2ba59ada386c6766faf
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

### `clojure:temurin-11-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:2d0cca0beb9faac7e117a41d4f1e16c4179cc77395128232627173f6771d72b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.6 MB (247581918 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:959781c7a8bfa72d54502e47ff99117654fa75ff3a3f10ceaf21befa1b7ca8fe`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1769990400'
# Thu, 05 Feb 2026 23:03:28 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 05 Feb 2026 23:03:28 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 05 Feb 2026 23:03:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Feb 2026 23:03:28 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Thu, 05 Feb 2026 23:03:28 GMT
WORKDIR /tmp
# Thu, 05 Feb 2026 23:03:46 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 05 Feb 2026 23:03:46 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 05 Feb 2026 23:03:46 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:0c8d55a45c0dc58de60579b9cc5b708de9e7957f4591fc7de941b67c7e245da0`  
		Last Modified: Tue, 03 Feb 2026 01:15:17 GMT  
		Size: 29.8 MB (29778596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4621dbd8ed2d542e84da382b8990b754f8087cf239d75d8cfaa8142695316d21`  
		Last Modified: Thu, 05 Feb 2026 23:04:09 GMT  
		Size: 145.8 MB (145806888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af16c9d28bd29de8b999ddfaee7d9dcad02f6bfbd1ec637047dc89dabe23a91c`  
		Last Modified: Thu, 05 Feb 2026 23:04:07 GMT  
		Size: 72.0 MB (71995787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:771ad2cd8c8b70a97e18c639cbb5f821f16e81f5dd9f5a81728c1185d5a5c602`  
		Last Modified: Thu, 05 Feb 2026 23:04:04 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:b9ac3df7811b093187f43b1e41c54482253099ec567a5f4ecd06569c032bb4b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5291934 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf604642d13e006cce484c597e120eb8f6b6d1d3caf87a104ab24de121891ff3`

```dockerfile
```

-	Layers:
	-	`sha256:1b7882c769c6f7d986d180a5d9474307dbb603ad6c00d8f674dc20722345e00e`  
		Last Modified: Thu, 05 Feb 2026 23:04:05 GMT  
		Size: 5.3 MB (5277692 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f03d1c33704f3c5b810633f0b395c80134d0418738d0639f79e4ab00058ade47`  
		Last Modified: Thu, 05 Feb 2026 23:04:04 GMT  
		Size: 14.2 KB (14242 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:bdf77aec2f0d7192765165b8d320e9939caed5fe0563670cd8f1022b9f8f26fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.4 MB (244447926 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59bd69bb174bba6da0340fadc1c9e8473b9f815f86a22804bc7d3472388c5f25`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1769990400'
# Thu, 05 Feb 2026 23:04:35 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 05 Feb 2026 23:04:35 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 05 Feb 2026 23:04:35 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Feb 2026 23:04:35 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Thu, 05 Feb 2026 23:04:35 GMT
WORKDIR /tmp
# Thu, 05 Feb 2026 23:04:53 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 05 Feb 2026 23:04:53 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 05 Feb 2026 23:04:53 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:3ea009573b472d108af9af31ec35a06fe3649084f6611cf11f7d594b85cf7a7c`  
		Last Modified: Tue, 03 Feb 2026 01:15:22 GMT  
		Size: 30.1 MB (30140064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b76287ac775dd9f0e02f7653ebca044109e04fdf35778126e1b80d0b24c6e6a1`  
		Last Modified: Thu, 05 Feb 2026 23:05:19 GMT  
		Size: 142.5 MB (142500854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d9bb768f43e0ab8a55607dff66507a2a43574eeef94b284dfcc48e13d18a7f1`  
		Last Modified: Thu, 05 Feb 2026 23:05:18 GMT  
		Size: 71.8 MB (71806363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ce9554872e78626c52810a05f0d7f8354c8f025acf9e1d910d8aade3c4b6504`  
		Last Modified: Thu, 05 Feb 2026 23:05:15 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:9729ed218d5d0315696fc908f929d9eb00b7722285413fc8122c1de62a573a6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5298440 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eaa8c71d6ae9e7db600b2b92f235ee78163b1e1a5ad21634e07ad01901f8957b`

```dockerfile
```

-	Layers:
	-	`sha256:cd7ad2b0726a7622430f61baaf58712c6300d717fab85a092f9e6f18fdccb2f6`  
		Last Modified: Thu, 05 Feb 2026 23:05:15 GMT  
		Size: 5.3 MB (5284079 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e727d39112ad927cf1734a071540658d65833d3fa7057fa7d0d6fd58c1c7f82a`  
		Last Modified: Thu, 05 Feb 2026 23:05:14 GMT  
		Size: 14.4 KB (14361 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:97b2b623ab497385ba7c8b2ca35b4a56c7694df74b56a74857c01f6a46d941e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.0 MB (243987814 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e46d59a9bb2d7dd9346edef088535e0e1f4d4e21be3f25f26dc9f44d1b91d18`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1769990400'
# Fri, 06 Feb 2026 00:12:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 06 Feb 2026 00:12:52 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 06 Feb 2026 00:12:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Feb 2026 00:12:52 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Fri, 06 Feb 2026 00:12:52 GMT
WORKDIR /tmp
# Fri, 06 Feb 2026 00:20:41 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 06 Feb 2026 00:20:42 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 06 Feb 2026 00:20:42 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:1aee42d34fb7e3a2db6f83f2a84e17846ac990ed8ecf693a309ae759efdbdaa3`  
		Last Modified: Tue, 03 Feb 2026 01:16:35 GMT  
		Size: 33.6 MB (33600184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89289b5278c2f1609c295cb4cd096cadc38bc53f7e508544fffed72683f23a6f`  
		Last Modified: Fri, 06 Feb 2026 00:14:35 GMT  
		Size: 133.0 MB (132996872 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c0507c3fca3631274f89282aa19fc2c1e10041840eab1a6713b9dae6d739e63`  
		Last Modified: Fri, 06 Feb 2026 00:21:35 GMT  
		Size: 77.4 MB (77390112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fce7370eaf2f020b21d1f801669ce0b1a850beeb78b850e76d6dfa92d1f2a54b`  
		Last Modified: Fri, 06 Feb 2026 00:21:32 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:4041feccbd48880e839cd0468881f4be8c6199973b0a77b8e13a621266f03939
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5295739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dda42a17743c38875d8fc71050542b3ab23210e0d27385d1732a07af22e8432b`

```dockerfile
```

-	Layers:
	-	`sha256:58d4260aa3966c2c7ea9ad197f0493ce5fe74e3b5c8959687023eca276b5218a`  
		Last Modified: Fri, 06 Feb 2026 00:21:33 GMT  
		Size: 5.3 MB (5281448 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:47eebc9316e53464c9948814fb1cdd237c0be7568f6960739d360af272fef783`  
		Last Modified: Fri, 06 Feb 2026 00:21:32 GMT  
		Size: 14.3 KB (14291 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:fed780843937da2a7e5595cd547207a6a5b6b9fb5efece74ef8d3501846f6b90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.4 MB (229353998 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efde23269ceaa44ee7de017844a9efa4d5df4decf3d8b3c7f8e1687ab4682432`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1769990400'
# Thu, 05 Feb 2026 22:59:30 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 05 Feb 2026 22:59:30 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 05 Feb 2026 22:59:30 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Feb 2026 22:59:30 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Thu, 05 Feb 2026 22:59:30 GMT
WORKDIR /tmp
# Thu, 05 Feb 2026 23:01:33 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 05 Feb 2026 23:01:33 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 05 Feb 2026 23:01:33 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:809310277795fa02ff585c83bc37c8fb5e06066ee7e053bab5d08bf186beeae9`  
		Last Modified: Tue, 03 Feb 2026 01:14:11 GMT  
		Size: 29.8 MB (29838149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:200ff9b1aa1124336c2c7dc0004c611c54b740c820761788794b237ab27de521`  
		Last Modified: Thu, 05 Feb 2026 23:00:19 GMT  
		Size: 126.6 MB (126562175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88cd234813463746362434b79338f26aa817ad937044aadb145896e678203117`  
		Last Modified: Thu, 05 Feb 2026 23:01:58 GMT  
		Size: 73.0 MB (72953027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed90398140b69e0605431fca05df8ddd8d1965579b19b94eb93ab5665b72527f`  
		Last Modified: Thu, 05 Feb 2026 23:01:57 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:bc4da2a6dc7d14d7c6ef99a245292b01027c15ea2b637302daa512a762513569
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5287861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cab10792b1e041e388c807de53f59c5e7e0cf3dfbd3f0ee88fb9cb2d94ad1b6`

```dockerfile
```

-	Layers:
	-	`sha256:f5fa9ad4ca81a1cd7aca2010b64d3cbe3bd900644d24f3a79fa9ed9e44897986`  
		Last Modified: Thu, 05 Feb 2026 23:01:57 GMT  
		Size: 5.3 MB (5273620 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2a352fd83c4d01492b86a8d098d1d6775e21db56fb8f8ca6f7e2933920215f0b`  
		Last Modified: Thu, 05 Feb 2026 23:01:57 GMT  
		Size: 14.2 KB (14241 bytes)  
		MIME: application/vnd.in-toto+json
