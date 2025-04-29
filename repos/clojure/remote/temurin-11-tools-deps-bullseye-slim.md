## `clojure:temurin-11-tools-deps-bullseye-slim`

```console
$ docker pull clojure@sha256:169f809ef7fb366ff22779d9868d56fd0b570f6ec94702f40326c0e80975fbbe
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-tools-deps-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:b70753df6a78cc117424e54f24fff7ea23a0fa674fb7c076e716b32387884937
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.9 MB (234884078 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fa6ecda56846df24eb1805aaf06e390df9f20c778b9a423fa28e20ba0455e98`
-	Default Command: `["clj"]`

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
CMD ["clj"]
```

-	Layers:
	-	`sha256:c8e1eb8ab3b017bd9e33ddec83ebdd8292c542bbd14a8d5a6cfa2edc3ad3b8eb`  
		Last Modified: Mon, 28 Apr 2025 21:08:07 GMT  
		Size: 30.3 MB (30254604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98c383f0666f93eca3b75c433c19832872e702de8e0d9fed5f5e2a93475f2613`  
		Last Modified: Mon, 28 Apr 2025 22:07:03 GMT  
		Size: 145.6 MB (145635846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f07f826d0d9eb0dffa35281ca19b8079a75dd0216a258568c1561e5af50439a8`  
		Last Modified: Mon, 28 Apr 2025 22:07:01 GMT  
		Size: 59.0 MB (58992985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71c64535ac197f340a3e6f95bfc957ff8235e8afb24e1d4a905eb9a35a8931a9`  
		Last Modified: Mon, 28 Apr 2025 22:07:00 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:eac4a9d3e0971b6f1f86e06f094957c613060f30ad02f9eb50c3f75a23b7207f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5153518 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b967a0ba80a1a82737c0f86e7f594b368605eec7b1aa626a834247d2b8666952`

```dockerfile
```

-	Layers:
	-	`sha256:ad2d5696c7112f455048241ece16a500b559828c4bd5698b9cd802f6f83a2b13`  
		Last Modified: Mon, 28 Apr 2025 22:07:00 GMT  
		Size: 5.1 MB (5139208 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a9c37e90974b8a39519fe612b71632fc307f29a8f10c54319e415cc706a01b2d`  
		Last Modified: Mon, 28 Apr 2025 22:06:59 GMT  
		Size: 14.3 KB (14310 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:e926bee436a6a720e35876d5cf9dbc094b5b98e64b0411dd791effe52dd93f68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.3 MB (230299492 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3cd54f6c1951f353b24d827dea1210b098d9bc6cdd4df44c90f8da543a565fa3`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 26 Mar 2025 16:17:22 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1743984000'
# Wed, 26 Mar 2025 16:17:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 26 Mar 2025 16:17:22 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Mar 2025 16:17:22 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Wed, 26 Mar 2025 16:17:22 GMT
WORKDIR /tmp
# Wed, 26 Mar 2025 16:17:22 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:59627ca2e9712141a7d131bec6c9931f8ecea11eac34d96bd1213ccea68e18e5`  
		Last Modified: Tue, 08 Apr 2025 00:23:35 GMT  
		Size: 28.7 MB (28749498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ad1d14317d3a031e80061d38befa6227f9338c259b60edd4197d1dc2a8a7f1d`  
		Last Modified: Wed, 23 Apr 2025 18:14:17 GMT  
		Size: 142.4 MB (142422063 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a2a788faff615f6cb36adb4080398617c5f9684ba6090cc8cf3a6a9f51bc326`  
		Last Modified: Wed, 23 Apr 2025 19:43:09 GMT  
		Size: 59.1 MB (59127283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c629dea2a1e197fc82aed81f71a209a926b7b3407773f0a2e81dbb52156f4b3`  
		Last Modified: Wed, 23 Apr 2025 19:43:07 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:5b545165f8ba14c9388710fdcb686f4d7e729cbcad5189c0a74c13081012f49e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5159932 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4596d2544fff7c2113b2092728901afe81e1ce0df859334d2252e80b10f7a220`

```dockerfile
```

-	Layers:
	-	`sha256:f5d221947acae98e927fbda9f9e5c261ff7347eb189e179278793bfd30720511`  
		Last Modified: Wed, 23 Apr 2025 19:43:07 GMT  
		Size: 5.1 MB (5145504 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:624ced7807d0be3e607557aa81daf5ce4e9773312389f834dd74b03560e15c49`  
		Last Modified: Wed, 23 Apr 2025 19:43:07 GMT  
		Size: 14.4 KB (14428 bytes)  
		MIME: application/vnd.in-toto+json
