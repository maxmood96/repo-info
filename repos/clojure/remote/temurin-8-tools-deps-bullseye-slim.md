## `clojure:temurin-8-tools-deps-bullseye-slim`

```console
$ docker pull clojure@sha256:900a960afe20ee5bb2ed5d22a8cd46bb747dd6206b52129966cd729592f600e2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:ae8dd759dbc8be371391079689a20d5c1c21ed73309a2dff2bfd8a9d17716e8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.6 MB (192643294 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c347679ef24a9e538a8c9636059a2ce1cddd53ce835654a15c6e8953cda1c642`
-	Default Command: `["clj"]`

```dockerfile
# Thu, 03 Oct 2024 17:49:34 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1734912000'
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
	-	`sha256:6c87eefc1f428634061bcdc9ec95ccceecd7c7475d35a777479af83f64ee6915`  
		Last Modified: Tue, 24 Dec 2024 21:32:32 GMT  
		Size: 30.3 MB (30252643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d43847c8e4a95a5905b22ce29a2b2670b6ddb2002f50f0c8b5b3eb79c8e70ac`  
		Last Modified: Tue, 24 Dec 2024 22:37:28 GMT  
		Size: 103.6 MB (103633884 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8398e583aad7e32c781346280b3b589b95e18bba78897f41f2701f5daeab59f7`  
		Last Modified: Tue, 24 Dec 2024 22:37:27 GMT  
		Size: 58.8 MB (58756122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75f5c6c4a5c8cae82314108a37915401aa9cfe066c6b6e9ba6ffc7791d8a6678`  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:439539bd3a4685fb8739defcbc5c8316d5ca375f390eea58852660429ea08bc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5253521 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00954710659e6e577068e8292c4dac416d5f2f724596c9a34fa8f75097eaeb0c`

```dockerfile
```

-	Layers:
	-	`sha256:5fff89bc0e8cde6679f8591fd01279ad78718b12ca6b86c8189199588541ed7b`  
		Last Modified: Tue, 24 Dec 2024 22:37:27 GMT  
		Size: 5.2 MB (5239225 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d21d6eca60b99207e87a85fcb92777c1bbdd98cd8b2af198dbb41c12581be37d`  
		Last Modified: Tue, 24 Dec 2024 22:37:27 GMT  
		Size: 14.3 KB (14296 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:826ac6831048189f71e5331c47fee421ace29e1480acbe30f4b7e1cd6f3c190b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **190.4 MB (190373526 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73cac49c14dab361cfb3ddbbc13e2dbeaf1a4501270020152463fb1c069b37ae`
-	Default Command: `["clj"]`

```dockerfile
# Thu, 03 Oct 2024 17:49:34 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1734912000'
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
	-	`sha256:879a6187682fc52c69294a2f450abdb54e257a50e8133ec6e89cb140345be6ce`  
		Last Modified: Tue, 24 Dec 2024 21:34:50 GMT  
		Size: 28.7 MB (28744853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0955d514f6f2a289bad48cc1c4e8cae663c7421b08d1e1977c003b2d438c33b`  
		Last Modified: Wed, 25 Dec 2024 07:13:59 GMT  
		Size: 102.7 MB (102747715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2d6270f53f11e6d7750ff80f77a95d094cb16d3dd2a56adb644e4eb0d7bf8f8`  
		Last Modified: Wed, 25 Dec 2024 07:16:56 GMT  
		Size: 58.9 MB (58880315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6334c5446f1936cf57f2c3d08eed50d116efd4186c0f54ee4be1ceeb2cd3f5bb`  
		Last Modified: Wed, 25 Dec 2024 07:16:54 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:20d0de9f082f8aed8867d29118985f2df13c7c85e8500ec2409e059645d91efe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5260069 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22312e1d573ec4d3f7756d1959e2753b332ab3d47d81345584c76272b569e086`

```dockerfile
```

-	Layers:
	-	`sha256:dd6bff0975532e7cd636f6e2646bbedb095d0cb8823b459eacf47d1e1fe1c738`  
		Last Modified: Wed, 25 Dec 2024 07:16:55 GMT  
		Size: 5.2 MB (5245655 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c1e316d0d26388a33276e1bb00f576ca99a9f255db4927b084627ac648084346`  
		Last Modified: Wed, 25 Dec 2024 07:16:54 GMT  
		Size: 14.4 KB (14414 bytes)  
		MIME: application/vnd.in-toto+json
