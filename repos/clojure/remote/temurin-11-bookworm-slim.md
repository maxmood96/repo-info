## `clojure:temurin-11-bookworm-slim`

```console
$ docker pull clojure@sha256:646e932eaf88121ca6a252859a998c8e5c6e6fcaf8d02c55181bf9f085a8e13b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:2dbb302b879acac2d4dff686f4c91d46d159f24bb1d6b12dea62791ebb48df64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.2 MB (244159548 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c121ba4bb34a10b8b62788a6f2ec7a046dcaaea2650e5fe9cc2d96533caf41b5`
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
	-	`sha256:e2848db057425ff0c8639a36f4e83d857a99c66fe1268a8599f1952ea2fa1a2e`  
		Last Modified: Sat, 19 Oct 2024 02:55:31 GMT  
		Size: 145.5 MB (145549942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86b2624f555cb346abd68a39e06f066cb2683f59445f61aa32889fa5c2cdadff`  
		Last Modified: Sat, 19 Oct 2024 02:55:30 GMT  
		Size: 69.5 MB (69482674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b3aae174951581ae6dcca754b5324680dda79bbd297f554605470f53b8f13a3`  
		Last Modified: Sat, 19 Oct 2024 02:55:29 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:53462a9462a305f648ec76eae62ba5e591d888ad9a568212c108a9272ef75b62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4954907 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f346c80d51cd088d8d569c3449966458944ee3f87d28da6d30c24965909e9fd`

```dockerfile
```

-	Layers:
	-	`sha256:b97d7a12eb91c2612c23b6bfdc5a7da23ea0e9c5d8a53bc660cfebf205996fef`  
		Last Modified: Sat, 19 Oct 2024 02:55:29 GMT  
		Size: 4.9 MB (4940763 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0f54c2a5d21e4fb1bda647b8e6b169bd91c85e661c0dad81ea513504cb006e64`  
		Last Modified: Sat, 19 Oct 2024 02:55:29 GMT  
		Size: 14.1 KB (14144 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:e89bdf05b9d294fc850ef3e8d3b90bf2cb74f5799bcdce84c442db2e9ff57efe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.9 MB (240857178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:279a3b2f701ffe630f13bd40d40d07fad1efba9a36436eed9fc964ff011f1161`
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
	-	`sha256:7c6662f3a2b9a8c3547dd556f11c29ad4d8bafa4a8d2beccf7787b25b07805c8`  
		Last Modified: Sat, 19 Oct 2024 11:49:35 GMT  
		Size: 142.4 MB (142354834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc594d2addec718ac08a4a23d03a69e7d0ba5a8e85f5b0ce902bf4e727925c43`  
		Last Modified: Sat, 19 Oct 2024 11:55:06 GMT  
		Size: 69.3 MB (69345356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29e2bbdabcd329212e95986fb7ae5bf53da3789ad943ac40c12802f395e4a4c7`  
		Last Modified: Sat, 19 Oct 2024 11:55:04 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:837d6176cddfcef20b0dbed063e1ffade9b07609155b4b264bb33b733e2b6a6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4961404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea4b6c1d44047d5b8693804661264e8e7eeb4084b16ad6cff0b44fe3bf50c689`

```dockerfile
```

-	Layers:
	-	`sha256:bb582ee530ff089f172a152eb3033e02ed0784ee72be2d6cfceeb038bd52e721`  
		Last Modified: Sat, 19 Oct 2024 11:55:04 GMT  
		Size: 4.9 MB (4947148 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c502270dc776a477d3152a3e7a5a7dfecf6b0a8d83bacd2c095bc09219050817`  
		Last Modified: Sat, 19 Oct 2024 11:55:03 GMT  
		Size: 14.3 KB (14256 bytes)  
		MIME: application/vnd.in-toto+json
