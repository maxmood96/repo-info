## `clojure:temurin-11-bullseye-slim`

```console
$ docker pull clojure@sha256:614e61cc7e830b0b80b1e150fe451625a47375ef0f5047f9300527ab936e9c85
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:bc7ac4c83c8672298afd089e9eadba5f259ab239ad17f7139e37359a1601071b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.6 MB (234639973 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3c49ec6c5a992eed3efc1cd3611716cbb35b2f9fda53839bafce5cc33077add`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 29 Jan 2025 19:11:46 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1738540800'
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
	-	`sha256:cf799a8da63a7bb7f377162d10ed737dd26b0e1174c8ac5d89a5da6c15dc7c04`  
		Last Modified: Tue, 04 Feb 2025 01:36:33 GMT  
		Size: 30.3 MB (30252588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93c1ed3389592ebd62f037ed4217dbda6c5c503e15fe1229d040a3a0d9cb84ce`  
		Last Modified: Tue, 04 Feb 2025 05:21:08 GMT  
		Size: 145.6 MB (145598932 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b7a68aab7f5a04f545802d63736ccc8d758e4655709f04438da48dff98db3b8`  
		Last Modified: Tue, 04 Feb 2025 05:21:05 GMT  
		Size: 58.8 MB (58787810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e362232ac762ca552a2c550f67f74596f921d429a55084253da1c57b120e19bd`  
		Last Modified: Tue, 04 Feb 2025 05:21:04 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:950f5edde22d2055d747283a34658d338ed4e5b9b2f22bb7d8313d87b2a1846e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5151518 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cede56ddcddb000a96f515dfb7b925a2b1254a15651ad5daa62811a69fa8c20`

```dockerfile
```

-	Layers:
	-	`sha256:b1f45ecdbdc1754d3b6bcd5f1f3724988d001a04c5a6ad28663ceb7a0863b760`  
		Last Modified: Tue, 04 Feb 2025 05:21:04 GMT  
		Size: 5.1 MB (5137208 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:077b15c7b9b137d0eb7b1e8b3c82749b6f40bb9f4a8e3c33e9f0c0f98a37b5b0`  
		Last Modified: Tue, 04 Feb 2025 05:21:04 GMT  
		Size: 14.3 KB (14310 bytes)  
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
