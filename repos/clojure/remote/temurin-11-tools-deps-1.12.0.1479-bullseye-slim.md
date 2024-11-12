## `clojure:temurin-11-tools-deps-1.12.0.1479-bullseye-slim`

```console
$ docker pull clojure@sha256:974077f69835c5feec1fd4f9808b1093193fae658f0a21a823fc94eb5fa312ff
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-tools-deps-1.12.0.1479-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:03e605a471b447fb0cc319b34f66ab7e363e010a55f5966087af8e6ba090e154
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.8 MB (235793742 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f94cbe90c8562a0b9e3f840a66b97106b016625e254fcca7b004dacf31e56e8c`
-	Default Command: `["clj"]`

```dockerfile
# Thu, 03 Oct 2024 17:49:34 GMT
ADD rootfs.tar.xz / # buildkit
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
	-	`sha256:55ab1b300d4b4b00c98fb396b36f0f7ba5dab2f7d18927e3742d364632723cbe`  
		Last Modified: Tue, 12 Nov 2024 00:55:04 GMT  
		Size: 31.5 MB (31451561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df0f1f137ea0ef5feb9c5819dd9c391408efb151f5acf0107ce7f648e855ac11`  
		Last Modified: Tue, 12 Nov 2024 02:23:53 GMT  
		Size: 145.6 MB (145601317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a722cbe8b0e5596c8020bf7d2761b5d9d5a2cdca4051392ed6d47a21d751ea5`  
		Last Modified: Tue, 12 Nov 2024 02:23:51 GMT  
		Size: 58.7 MB (58740221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03350173f756c2aa27efc02cde05cb6c9905e8679125167b4cb70894c888effe`  
		Last Modified: Tue, 12 Nov 2024 02:23:50 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.0.1479-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:1e2da9c480c4fe0af4a1cd2bd13eca5ca6bb7bb188aa3635443283084f74af6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5159833 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:383caa2e375dbef2bd94ec610123871e7f9a7992ea120c8a0f08c20e4b5ba117`

```dockerfile
```

-	Layers:
	-	`sha256:53d8e77f049531ee1f87683bd672602908e9f4cf1a9b84bce5617e92199a8fa0`  
		Last Modified: Tue, 12 Nov 2024 02:23:51 GMT  
		Size: 5.1 MB (5145523 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a2f610198af06a4f2c27d22008df15fa16b3000431e1611972cf6024b16e8a2c`  
		Last Modified: Tue, 12 Nov 2024 02:23:50 GMT  
		Size: 14.3 KB (14310 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-1.12.0.1479-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:db9d59d994b2353d47d4472bec6c7dd545f1753595ae3a326a211324da55d2cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.8 MB (233762215 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5f8843eba6254b85983d01235ae155a5226e38394a1d8436bde803b970aab8f`
-	Default Command: `["clj"]`

```dockerfile
# Thu, 03 Oct 2024 17:49:34 GMT
ADD file:f3f9a52e18a8da911b50ebddcc922d4b5a7aa8caa6eb15fb5c26c696b8fe9610 in / 
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
	-	`sha256:b3c56a24ca3234ee90349473402ac1b368a2fb3c9620242fa70a85d7396d7799`  
		Last Modified: Thu, 17 Oct 2024 01:15:14 GMT  
		Size: 30.1 MB (30075757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3d15ddb0fe087446fc432cc41ac41015a1aaa06bd765a4885778025f96eacd6`  
		Last Modified: Thu, 24 Oct 2024 03:44:24 GMT  
		Size: 142.4 MB (142389106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:979441870ceaff144a1da3d276d563b066ea40a9b975d1c58674d8e83a1733aa`  
		Last Modified: Thu, 24 Oct 2024 09:11:25 GMT  
		Size: 61.3 MB (61296709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f0d346b7b94b9125c7b4255190083bba49d2e464004da994e39bf903dbd25f9`  
		Last Modified: Thu, 24 Oct 2024 09:11:23 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.0.1479-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:36e92cbf04667905ddbed64975dae8392db6364cd8aea06c0c2b7c0036b78c64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5166099 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:154f8a5afe98d2278418d661cf579c7d35ce7e3d3a9e34546b92dddd2ab8e727`

```dockerfile
```

-	Layers:
	-	`sha256:4f0accf7059ee494d7823bdb9d0e2f7e8a191637993e87469cf28a56ad57a8e4`  
		Last Modified: Thu, 24 Oct 2024 09:11:24 GMT  
		Size: 5.2 MB (5151843 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d57399c331be5de897c43c95d1544c6ebf9740127c0b04c33a243efaaa2a31ce`  
		Last Modified: Thu, 24 Oct 2024 09:11:23 GMT  
		Size: 14.3 KB (14256 bytes)  
		MIME: application/vnd.in-toto+json
