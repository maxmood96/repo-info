## `clojure:temurin-17-bookworm-slim`

```console
$ docker pull clojure@sha256:2731f09f2090bcb4d3bd93153b3020d9b5ba9b27c0ca3b9dbba21d67af936721
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:3c3182909d3838784365b16e5b1557815d83a9e774b04609cc87485cff4e837c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.8 MB (243776834 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fd340c212fcfab2665ce9300a9137cb001e22c41409e1ccbfa3a70708b353f3`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

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
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:a480a496ba95a197d587aa1d9e0f545ca7dbd40495a4715342228db62b67c4ba`  
		Last Modified: Thu, 17 Oct 2024 00:23:58 GMT  
		Size: 29.1 MB (29126289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f50f7ba52775b32a2205d6843073aa6334c5121d75aa12fd9b9bc9239cb50998`  
		Last Modified: Sat, 19 Oct 2024 02:57:27 GMT  
		Size: 145.2 MB (145166530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54d17797e91cd9114adeb3b3eda745ed508ccb68d7c2012590dfecf44daac66d`  
		Last Modified: Sat, 19 Oct 2024 02:57:22 GMT  
		Size: 69.5 MB (69482976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba022263727756cb55be3b3e133d9af3bbc199e55ef55f051d249dcb75bcbf56`  
		Last Modified: Sat, 19 Oct 2024 02:57:21 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8dcab0203a3708c75ad3b63ea9adcdca5831502ed67834a30c4e7b52433c46d`  
		Last Modified: Sat, 19 Oct 2024 02:57:21 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:e81ce1009d2648d7090b5f7bcbd5f689ede478869999ee658573d20467667af9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4935675 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb67e661bd8aa04cbc517bd8f862c628bbd9075d2f2001e14d24776c0dc91c50`

```dockerfile
```

-	Layers:
	-	`sha256:79c1bf89523b1dd9f2a1f252caca2d3defc117b6e769cdf138a229494e82e985`  
		Last Modified: Sat, 19 Oct 2024 02:57:21 GMT  
		Size: 4.9 MB (4919956 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f6a6a8fed5c398fee223ddf5ce85e6ac2468ca9076fa2312849be0f951f64c2d`  
		Last Modified: Sat, 19 Oct 2024 02:57:21 GMT  
		Size: 15.7 KB (15719 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:d20d421dea8ac18cf0213a9b81cd0d68654e4a2e13450f71a9cf187298dc28af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.5 MB (242462063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d36cd000afa7e4bf1273a102beade95f67c0e10f7e6a3b61553c161463aef3ff`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

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
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:83d624c4be2db5b81ae220b6b10cbc9a559d5800fd32556f4020727098f71ed0`  
		Last Modified: Thu, 17 Oct 2024 01:14:39 GMT  
		Size: 29.2 MB (29156341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:467c862b0e10aff6a74318a3baf39f91f14902d551963d4cac1c395597956120`  
		Last Modified: Thu, 17 Oct 2024 08:12:42 GMT  
		Size: 144.0 MB (143959463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf77ef51da65e55f40f4febaf475a8c3f6ac8ca4bab6afbb717037520a6ad9b2`  
		Last Modified: Thu, 17 Oct 2024 08:16:48 GMT  
		Size: 69.3 MB (69345219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe1f02fcad5fe0c361a480d0ff6aa4902ba626e83f841579243d69ead7b6dea5`  
		Last Modified: Thu, 17 Oct 2024 08:16:46 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3182514c12b3d07ab0efdf12c5036864af593a7cf6c2f9ca0e5f39058e7b4afc`  
		Last Modified: Thu, 17 Oct 2024 08:16:46 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:668a69cfa85b56fc0487f530f1bc0011ef5c98c5c7aa151b0a643d60ce57d61c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4915632 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:590805ca798a222ab03f2cc1ace1a9936d3dde3fe2757b3f44b0821c7db6032e`

```dockerfile
```

-	Layers:
	-	`sha256:b9c82f92d1b936d4bc57063c73926ef3bd67c9a9e68f21fd6983cd804f9e0e0a`  
		Last Modified: Thu, 17 Oct 2024 08:16:46 GMT  
		Size: 4.9 MB (4899977 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:643a460614005ad11ea4ebff6c1c6c2c3d5969d04c1431e8f6551dec9325168f`  
		Last Modified: Thu, 17 Oct 2024 08:16:46 GMT  
		Size: 15.7 KB (15655 bytes)  
		MIME: application/vnd.in-toto+json
