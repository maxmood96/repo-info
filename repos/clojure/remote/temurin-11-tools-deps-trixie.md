## `clojure:temurin-11-tools-deps-trixie`

```console
$ docker pull clojure@sha256:05f98d5b3b53f4e87ea3cdfd0d0e044062e80b555d65b995c8e32a957d87c028
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

### `clojure:temurin-11-tools-deps-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:b8b5b30d38977eeb4b1314adf0ebab0515567a5c7bd9572de1e5750996098933
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **283.4 MB (283441270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:957a59ee56009663c91dd968adbcec0913e2c5a9ebda0c09d47c97ec788d6cee`
-	Default Command: `["clj"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1759104000'
# Fri, 26 Sep 2025 15:53:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 26 Sep 2025 15:53:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Sep 2025 15:53:20 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 26 Sep 2025 15:53:20 GMT
WORKDIR /tmp
# Fri, 26 Sep 2025 15:53:20 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:cae3b572364a7d48f8485d67baee38e4e44e299b8c8c4d020ff7fb5fdd97f88c`  
		Last Modified: Mon, 29 Sep 2025 23:35:29 GMT  
		Size: 49.3 MB (49284626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f2ac2f9374acaa03c35a04ba2f4a127db89dd2f7d416ca0a432a60a09b89bff`  
		Last Modified: Thu, 02 Oct 2025 13:12:46 GMT  
		Size: 145.7 MB (145658171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbf3bc087ef2006b8a57c8aad4e9d42476a06dff98c060435b6bb66f0e9897c7`  
		Last Modified: Thu, 02 Oct 2025 08:58:12 GMT  
		Size: 88.5 MB (88497830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb6d307962cac8205b15ac8a3099939e5e9da2c2e08bba9573c99992990f4f3e`  
		Last Modified: Thu, 02 Oct 2025 08:58:01 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:68ecc0b0f8f95e9c4b982e2498551353a9bb43f6e5887385b7ed27e5b4fcddad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7501268 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6823bb8db1c5e9608c25e5dd9ed867efe86ed846537f53e4e7adb5d7dd8eddc5`

```dockerfile
```

-	Layers:
	-	`sha256:8a264bad86c4de1b05613ae49722e0337bd88ea05c2471f860672aa2da9a81ee`  
		Last Modified: Thu, 02 Oct 2025 12:37:22 GMT  
		Size: 7.5 MB (7487040 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:18e13b2ccd3e6e5af6c8c3f28ffa7c419d076e69cf24f361672e4c2765635d8c`  
		Last Modified: Thu, 02 Oct 2025 12:37:23 GMT  
		Size: 14.2 KB (14228 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:8993fad77738b63c0fe70fa6060d935dceb61315637227b0a47e8b337f4358b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.8 MB (280798556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f41c69e2ce6e20a9d1436815d7a3858bf7ed81fd05afa136b4920f5d8412ef6f`
-	Default Command: `["clj"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1759104000'
# Fri, 26 Sep 2025 15:53:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 26 Sep 2025 15:53:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Sep 2025 15:53:20 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 26 Sep 2025 15:53:20 GMT
WORKDIR /tmp
# Fri, 26 Sep 2025 15:53:20 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:28aec8b14b3eeacbf47ef38af72fab694b109fdcdf31581722750599baf1a932`  
		Last Modified: Mon, 29 Sep 2025 23:35:17 GMT  
		Size: 49.6 MB (49648695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7aedafb01281150d9db9e6e9d6c2e09103659a50e2e22fc69df57d91f256ae89`  
		Last Modified: Thu, 02 Oct 2025 02:42:47 GMT  
		Size: 142.5 MB (142458700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:533490a2b7d496eda0573a31e6c7352239dddf0c2097f59276950799d765fe2d`  
		Last Modified: Thu, 02 Oct 2025 02:42:58 GMT  
		Size: 88.7 MB (88690516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36eff25a4057b33f49352bf95e63a794e0f9041a15e77a671697b7e6e4fb5824`  
		Last Modified: Thu, 02 Oct 2025 02:42:54 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:8d219dda4c8504cf7797e59dc1b0c536f450ef7ba751331347cf4138a08c92fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7509034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b73e2e62fab4cb405acc5db712b68e967d656caaf9ae6a66ea58c79384280569`

```dockerfile
```

-	Layers:
	-	`sha256:be564c894bb6728d1d1104646e4c60b2e35e8a2641fdb3c6beddb5187670a1f2`  
		Last Modified: Thu, 02 Oct 2025 06:38:13 GMT  
		Size: 7.5 MB (7494688 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:36d14420443e05578b434806d97b49e1ea8449581d93d85461335cd27f33da86`  
		Last Modified: Thu, 02 Oct 2025 06:38:14 GMT  
		Size: 14.3 KB (14346 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:eab582e179d87c7cf87503dd6e17bcb8b622ea9fe426b3167b8825ad489d1378
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.1 MB (280115174 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2b7d9fac98b0676a294f185f2beaeb562f27445f5ca98e9e8d5ddf67fa99b8a`
-	Default Command: `["clj"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1759104000'
# Fri, 26 Sep 2025 15:53:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 26 Sep 2025 15:53:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Sep 2025 15:53:20 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 26 Sep 2025 15:53:20 GMT
WORKDIR /tmp
# Fri, 26 Sep 2025 15:53:20 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:71fbf24a239310917388930bb043e64907cb532b9ac8f265e44e032dc3bf4409`  
		Last Modified: Mon, 29 Sep 2025 23:41:05 GMT  
		Size: 53.1 MB (53109217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d160fe717ff6366feacf5df22ac8b1d697719e1e16e7df4f77fab938a3f192f1`  
		Last Modified: Thu, 02 Oct 2025 08:27:28 GMT  
		Size: 132.9 MB (132853321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b876f609264a84d50bd1186d970c6152dd380f5c2fe7e8e2f116bb5c7888a32`  
		Last Modified: Thu, 02 Oct 2025 08:39:28 GMT  
		Size: 94.2 MB (94151990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bff9bb339d959157d3852324a2096b2291b4d8c209e2e62774beb3a95388584c`  
		Last Modified: Thu, 02 Oct 2025 08:39:24 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:54f8e9efe4cf0372b3396e8642ea4543a4386999c86fda2899e0d25b4a4f0f86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7505120 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a36233460177ceb01729e0eb9fafc495c020118dc7be122d72e5c476405b5bb`

```dockerfile
```

-	Layers:
	-	`sha256:eafe2eb1fd6aa13f3301f6e3f7ba00ee73264d1261840ab84231014752a77bae`  
		Last Modified: Thu, 02 Oct 2025 09:36:37 GMT  
		Size: 7.5 MB (7490844 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5018a8459cfdc2cc8dcc911dfcec60066ff8e80149f3c960bc4cd88a3d232ada`  
		Last Modified: Thu, 02 Oct 2025 09:36:39 GMT  
		Size: 14.3 KB (14276 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:d7d15850500168b5bc118f724a70c12322289291145fe5c7df1b5148de63e479
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **264.1 MB (264098251 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c122a8be0596ab922155cba0f662c4597aa6268cb9f4a958e42dbe96bfaf1e1`
-	Default Command: `["clj"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1759104000'
# Fri, 26 Sep 2025 15:53:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 26 Sep 2025 15:53:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Sep 2025 15:53:20 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 26 Sep 2025 15:53:20 GMT
WORKDIR /tmp
# Fri, 26 Sep 2025 15:53:20 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:024d6c344f0b9dbb2baf07e95dfd2abbfadc5c8262ca381f39f6489670cbaff5`  
		Last Modified: Mon, 29 Sep 2025 23:41:06 GMT  
		Size: 49.4 MB (49351442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0915508be4a922738aba0ff6e827cf11c307f386543badcd8e0d6e1cfee0e13f`  
		Last Modified: Thu, 02 Oct 2025 04:22:03 GMT  
		Size: 125.6 MB (125621606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:849a19dcb1d1063fb9c006f0d601d5e7ad46c2665bff2483a90a0be0fbeffe07`  
		Last Modified: Thu, 02 Oct 2025 04:28:05 GMT  
		Size: 89.1 MB (89124559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cb2985761a6635ac9425f383e5e02239baaec6fa7bfdcfe8815f80310e710f5`  
		Last Modified: Thu, 02 Oct 2025 04:28:00 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:f52f9e8eb7be53a1cd952a80dc49ff5c2e21e8dfa75fc64f9fce2c543e004d41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7497194 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08eb9e2ae221a96cef29b073efa316a53e683a9cd7e5756ae49d93049eb57b41`

```dockerfile
```

-	Layers:
	-	`sha256:88d452a530cb6b0725bdcbed2a99cde7c86527f71ebc0b2541868f190dc07d72`  
		Last Modified: Thu, 02 Oct 2025 06:38:22 GMT  
		Size: 7.5 MB (7482966 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0b2409f6c20f7fcc2d6de31581e23af334e1e3633f34782147c755b0f7925ac5`  
		Last Modified: Thu, 02 Oct 2025 06:38:23 GMT  
		Size: 14.2 KB (14228 bytes)  
		MIME: application/vnd.in-toto+json
