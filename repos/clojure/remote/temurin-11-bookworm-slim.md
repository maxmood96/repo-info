## `clojure:temurin-11-bookworm-slim`

```console
$ docker pull clojure@sha256:933d7554da0be2988a1d390c9e901f42f64ef9e45317855d3969a56a6c9568c7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:e15898c75dace33cfc509a1fb015bac437eadab7f6ea78c4b14621419e759631
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.2 MB (244210906 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2689d140059697883c67e1b31c69251add4e9e938c3a78c4058d53396a7afbec`
-	Default Command: `["clj"]`

```dockerfile
# Thu, 03 Oct 2024 17:49:34 GMT
ADD file:90b9dd8f12120e8b2cd3ece45fcbe8af67e40565e2032a40f64bd921c43e2ce7 in / 
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["bash"]
# Thu, 03 Oct 2024 17:49:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 03 Oct 2024 17:49:34 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Oct 2024 17:49:34 GMT
ENV CLOJURE_VERSION=1.12.0.1479
# Thu, 03 Oct 2024 17:49:34 GMT
WORKDIR /tmp
# Thu, 03 Oct 2024 17:49:34 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "94f29b9b66183bd58307c46fb561fd9e9148666bac13a4518a9931b6f989d830 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:a480a496ba95a197d587aa1d9e0f545ca7dbd40495a4715342228db62b67c4ba`  
		Last Modified: Thu, 17 Oct 2024 00:23:58 GMT  
		Size: 29.1 MB (29126289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1794becafd5976b4f5cc63b358d1e37d6ecf911f0cf1a750a6a9dfe63ce43127`  
		Last Modified: Thu, 24 Oct 2024 02:00:03 GMT  
		Size: 145.6 MB (145601283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf06793d77e6bc36351105968eebf82b95ce3ed09b1e5ff00ab5d5e5b37a0827`  
		Last Modified: Thu, 24 Oct 2024 02:00:01 GMT  
		Size: 69.5 MB (69482688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72e3fce16babb83e636649d69b770128bbe330cabc41d48581bfaca40acd0c62`  
		Last Modified: Thu, 24 Oct 2024 01:59:58 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:97c3e8ec1773a5080f42512707ca3d00c641ffc5de22349733549f5ba22f7fd0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4954877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c94654d0ff6b48ae1a3c7a077dbaa48d1b550374afd71614ca9eb05c89d98880`

```dockerfile
```

-	Layers:
	-	`sha256:bfe456a55979c1f339bd86efc74ff76a052e71509856e37bb232019d8eb15718`  
		Last Modified: Thu, 24 Oct 2024 01:59:59 GMT  
		Size: 4.9 MB (4940763 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8d5e786ec21b291a6d94833e99388444b0dacf0a5bb5518e38cefba2ae904122`  
		Last Modified: Thu, 24 Oct 2024 01:59:58 GMT  
		Size: 14.1 KB (14114 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:e5c077f3cc72d59ca5166f29f5411c45f51c8c0bfc425b00cf4f7e0e05c3bb5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.9 MB (240891496 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26d5aa3e982f979d88a41e5d9b35d93e61140613477508c92321364fccb141ab`
-	Default Command: `["clj"]`

```dockerfile
# Thu, 03 Oct 2024 17:49:34 GMT
ADD file:702193928cded0bcec5edbf4a5660961e7caef8c9d9cafea3337b7f6720c4464 in / 
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["bash"]
# Thu, 03 Oct 2024 17:49:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 03 Oct 2024 17:49:34 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Oct 2024 17:49:34 GMT
ENV CLOJURE_VERSION=1.12.0.1479
# Thu, 03 Oct 2024 17:49:34 GMT
WORKDIR /tmp
# Thu, 03 Oct 2024 17:49:34 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "94f29b9b66183bd58307c46fb561fd9e9148666bac13a4518a9931b6f989d830 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:83d624c4be2db5b81ae220b6b10cbc9a559d5800fd32556f4020727098f71ed0`  
		Last Modified: Thu, 17 Oct 2024 01:14:39 GMT  
		Size: 29.2 MB (29156341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f9c9542bb5c24b01cc4444fc921ba60e64bde0acc844aa27de102d3306ab810`  
		Last Modified: Thu, 24 Oct 2024 09:04:12 GMT  
		Size: 142.4 MB (142389159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:994ae9f49fa9841ade8271e455e18d7ca999faa1d0806d5e4d7d320a06096e5f`  
		Last Modified: Thu, 24 Oct 2024 09:09:46 GMT  
		Size: 69.3 MB (69345350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcda3d8c86dedcb38ce900a99fb66e6511adca034d8f98bb1215d8724bd77dbb`  
		Last Modified: Thu, 24 Oct 2024 09:09:44 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:95ef02538c69fb59eea9d43b4605f0f2154f9c3b61f00371502ad4f7f325b00c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4961402 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2bbd7eeaf963cda30885faa12beb108b8e831f8cc4f8c0fd2347cce3f62bf31`

```dockerfile
```

-	Layers:
	-	`sha256:cb73bc7a894c98d2469bc4f7d625491888b5cb8721db099dec5d93da8ad5d5b1`  
		Last Modified: Thu, 24 Oct 2024 09:09:44 GMT  
		Size: 4.9 MB (4947148 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3d6780393282137e0d6c50fa2e74dc74dbdbefe0786a78197093001012f9a035`  
		Last Modified: Thu, 24 Oct 2024 09:09:43 GMT  
		Size: 14.3 KB (14254 bytes)  
		MIME: application/vnd.in-toto+json
