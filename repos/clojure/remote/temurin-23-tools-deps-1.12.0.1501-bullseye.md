## `clojure:temurin-23-tools-deps-1.12.0.1501-bullseye`

```console
$ docker pull clojure@sha256:936d1901af2997da0b9835f355e0e3d00600a51b457881ebd46e080487366098
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-23-tools-deps-1.12.0.1501-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:39eabece1f1557a9003bf5552279143c63edd77111650aad72bcf9b2907dcbab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.2 MB (288247278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0a411684bb16da33b170bc93c7908bc4774f6ef68e10ee0a9d860eb56474741`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

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
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 29 Jan 2025 19:11:46 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 29 Jan 2025 19:11:46 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:de97e8062e06250e3c3cef0d40cfe62111bb4b74bcf6221e25a06452dacffcf6`  
		Last Modified: Tue, 14 Jan 2025 01:33:36 GMT  
		Size: 53.7 MB (53739164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:783e18a15e17761df10a58720edf6cb857a58d0cbc3be405874d346f467c2327`  
		Last Modified: Fri, 31 Jan 2025 02:18:46 GMT  
		Size: 165.3 MB (165316176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eac180782c77da5c4a7fdead2f86f7595764e18b2c2778e04c4f11dba1acb44a`  
		Last Modified: Fri, 31 Jan 2025 02:18:44 GMT  
		Size: 69.2 MB (69190896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53e18720db1876b0df967b65131047b46bc4a5c8150f271a5f01b8e8a29aa62b`  
		Last Modified: Fri, 31 Jan 2025 02:18:41 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e08bcd085c50c15db4c4b648342f0d7c9cdda5ef73ed1b7c2e3ffd9a2f64fee`  
		Last Modified: Fri, 31 Jan 2025 02:18:41 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-23-tools-deps-1.12.0.1501-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:362f854bc0245e848abe80e2e3dba69c0b98be331511eafb91b45a09052c2e2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7225380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb95ed7a087807817f67fcd61496db058fdbf1654156603e54fb0610e9642d11`

```dockerfile
```

-	Layers:
	-	`sha256:e7cd74830c673003054daac54a57f5899212eee854cc3abfcbd790738c9af360`  
		Last Modified: Fri, 31 Jan 2025 02:18:42 GMT  
		Size: 7.2 MB (7209560 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7eb46822258b9c6a7eddd53528bf4795112cfe40afe20cbea20feaf7b4056c5a`  
		Last Modified: Fri, 31 Jan 2025 02:18:41 GMT  
		Size: 15.8 KB (15820 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-23-tools-deps-1.12.0.1501-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:3e6b5ac66115783e67ed041431b9c980968ecd88ec12d89455b7078ca11d4eb1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.8 MB (284840339 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74f6c09c828c66ce67dd3f177c19f97bdb108dde8d0d95bf1e844850f93dd65b`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

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
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 29 Jan 2025 19:11:46 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 29 Jan 2025 19:11:46 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:1270858b2b9cb5d47abd119b946534b70ff7d09f29c425fc07b280e5c28971c6`  
		Last Modified: Tue, 14 Jan 2025 01:36:12 GMT  
		Size: 52.2 MB (52246060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77ca543c77f30c2f45d64e12050b7d093e1c0ddaf3c74b92fda20bba862b0f7d`  
		Last Modified: Thu, 23 Jan 2025 03:55:52 GMT  
		Size: 163.3 MB (163281769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30181f9b9171237018058a8a8ae6d33794791b431bce8990cbbee8ba001a32a7`  
		Last Modified: Wed, 29 Jan 2025 20:59:20 GMT  
		Size: 69.3 MB (69311468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef7ffc29c2a72a870830bd2aa3796a3460d59569456337a1c517659dd94f40eb`  
		Last Modified: Wed, 29 Jan 2025 20:59:18 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edf93e6ae0d3745994323c0e49ef0bf96c5571215f51d76c9583aa1a0f6d18c0`  
		Last Modified: Wed, 29 Jan 2025 20:59:18 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-23-tools-deps-1.12.0.1501-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:3e8d3f008e543d0d86739b92b29b8d5f1b644e36556a5be85dd5eb4c8b964a3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7229978 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3516e794c1060985d09ad494ebaf9e0012d83320e5bfc9f7a3538f6f412ea113`

```dockerfile
```

-	Layers:
	-	`sha256:b54ee27a1b52d865f2d920f57522d9e4661866b42a5f9471f8ff0d6e9775bb2d`  
		Last Modified: Wed, 29 Jan 2025 20:59:18 GMT  
		Size: 7.2 MB (7214040 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4a86214c01192b32f300b0c66c3a40a1ca11f8e292eea74cb8eaf7c416fc991d`  
		Last Modified: Wed, 29 Jan 2025 20:59:17 GMT  
		Size: 15.9 KB (15938 bytes)  
		MIME: application/vnd.in-toto+json
