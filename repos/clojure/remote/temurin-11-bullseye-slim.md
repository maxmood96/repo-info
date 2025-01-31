## `clojure:temurin-11-bullseye-slim`

```console
$ docker pull clojure@sha256:c60a9628ff94daf9dad6b6e1e2584fcb4951aca387920e73812db247476b4f53
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:53e17d287f33251dadd63b8eda80c8e96630a4110a86848071e4cf97870983aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.6 MB (234639947 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fda0e86a9e01572c7999be95529b45cbdddfeb478fe97ee5d6986a8e54bb05dd`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1736726400'
# Wed, 29 Jan 2025 19:11:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 29 Jan 2025 19:11:46 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 29 Jan 2025 19:11:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 29 Jan 2025 19:11:46 GMT
ENV CLOJURE_VERSION=1.12.0.1501
# Wed, 29 Jan 2025 19:11:46 GMT
WORKDIR /tmp
# Wed, 29 Jan 2025 19:11:46 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "65257085958376a3c89755a6108d67163882c75af709fe8c8918222ca5730aef *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 29 Jan 2025 19:11:46 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 29 Jan 2025 19:11:46 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:89320e7119e225692d79aaeb4989a18d7f97daafdb2b3782f84a0a8de31a09de`  
		Last Modified: Tue, 14 Jan 2025 01:33:29 GMT  
		Size: 30.3 MB (30252665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d9bbfc938bd05d7c029999f0da0130054fe5387c577527fb8cf9c9e5ae4518e`  
		Last Modified: Fri, 31 Jan 2025 02:17:36 GMT  
		Size: 145.6 MB (145598795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eda6690210c326a30701d94652feef5cec7e57c359594d18e75cbc5197be4ab0`  
		Last Modified: Fri, 31 Jan 2025 02:17:34 GMT  
		Size: 58.8 MB (58787841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:097ae7999efb5c1c5bde516f12ff17f823b63e4755844f96fb6adf3dce74b21e`  
		Last Modified: Fri, 31 Jan 2025 02:17:33 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:0f02b4b5f55f5927e79929a39464b0be652778b24f6593bbcdd9081039f00566
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5151517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:705ea2b92b6359eefb8d9f570e1d867618baf94f0a787c75f718e0a92a949415`

```dockerfile
```

-	Layers:
	-	`sha256:b6138abaf033bc1d1e4a213ef066df619efb0b012156b16c6b5c182e478999d9`  
		Last Modified: Fri, 31 Jan 2025 02:17:33 GMT  
		Size: 5.1 MB (5137208 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0a47b72b0eeb8fa47b90de2551467002df0f9d8909b0066bf89f8369b8d29462`  
		Last Modified: Fri, 31 Jan 2025 02:17:33 GMT  
		Size: 14.3 KB (14309 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:5b3757e324de238bdbba92266370b8fa460e2289c4afadc8dd17120b58919a10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.0 MB (230040095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48d5f8dd714cbbe5546db3bbbf0927cd27be25d5f507a24c372fd9fcd1ff2515`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1736726400'
# Wed, 29 Jan 2025 19:11:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 29 Jan 2025 19:11:46 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 29 Jan 2025 19:11:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 29 Jan 2025 19:11:46 GMT
ENV CLOJURE_VERSION=1.12.0.1501
# Wed, 29 Jan 2025 19:11:46 GMT
WORKDIR /tmp
# Wed, 29 Jan 2025 19:11:46 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "65257085958376a3c89755a6108d67163882c75af709fe8c8918222ca5730aef *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 29 Jan 2025 19:11:46 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 29 Jan 2025 19:11:46 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:6a43d3167ec1fb9f3b40bf3e095c86abebf31d406e2de1d196433c26d262f72c`  
		Last Modified: Tue, 14 Jan 2025 01:36:26 GMT  
		Size: 28.7 MB (28744913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e75f2a1647a2213cea5bd866fc62a6cb80c08c0c97a030b53f5ae8e5be7bc170`  
		Last Modified: Fri, 31 Jan 2025 03:36:23 GMT  
		Size: 142.4 MB (142385501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef08da2131a03e76caed6ecd959afb200ed9c36d700449da4df2c0e94a6f48a6`  
		Last Modified: Fri, 31 Jan 2025 05:08:01 GMT  
		Size: 58.9 MB (58909035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e2ff44d6b17348c8e17656bcfe92b50f603d392a4187c5e2961def68970c0c9`  
		Last Modified: Fri, 31 Jan 2025 05:07:58 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:c92268dff90adeaee90f1c272d72141d5d21d38ec3d463a834d466eef8e4c2c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5157985 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94c44f88783a91767318fb2c28ec18108c9ea383fe8912e1105d6cf55afe8ed6`

```dockerfile
```

-	Layers:
	-	`sha256:0674dac6bc3288632e261f20adf68594d9c6549bb67a5ca73ab6ec1acbd04ab8`  
		Last Modified: Fri, 31 Jan 2025 05:07:58 GMT  
		Size: 5.1 MB (5143558 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4bff142d498eae265b05f4aabe148593ae80f513e11c65b8d1983338c9895bea`  
		Last Modified: Fri, 31 Jan 2025 05:07:58 GMT  
		Size: 14.4 KB (14427 bytes)  
		MIME: application/vnd.in-toto+json
