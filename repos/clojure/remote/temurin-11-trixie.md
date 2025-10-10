## `clojure:temurin-11-trixie`

```console
$ docker pull clojure@sha256:c4ad04c24aac973fa272ad9285afeedb5e0fb65c5b1624e09d37864a4d9e1d7c
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

### `clojure:temurin-11-trixie` - linux; amd64

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

### `clojure:temurin-11-trixie` - unknown; unknown

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

### `clojure:temurin-11-trixie` - linux; arm64 variant v8

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
		Last Modified: Fri, 03 Oct 2025 08:59:57 GMT  
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

### `clojure:temurin-11-trixie` - unknown; unknown

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

### `clojure:temurin-11-trixie` - linux; ppc64le

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
		Last Modified: Sun, 05 Oct 2025 11:51:37 GMT  
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

### `clojure:temurin-11-trixie` - unknown; unknown

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

### `clojure:temurin-11-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:55b6bcaee8da1c695ac5b19d87f3325e738928bf0eabb32d71d68a9ebd154987
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **264.1 MB (264099411 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d158caf78426bcf85df577a641deebeda971fe5861f1e3aa18ab2cd6a7a1f31`
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
	-	`sha256:f84f66a0fc9c354ca1f63065e761ed625868322e7e3a30084169fe6d34e33876`  
		Last Modified: Thu, 09 Oct 2025 22:54:23 GMT  
		Size: 125.6 MB (125622160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d22cf04f3c08df2823ca8a1f1641181924d46b50609de21210d4ec089ebfaff3`  
		Last Modified: Thu, 09 Oct 2025 23:06:12 GMT  
		Size: 89.1 MB (89125164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e046f6c8357e5e2bbb4effa2c268362293a5af2fb84636cacdab97b7e8f82d8f`  
		Last Modified: Thu, 09 Oct 2025 23:06:05 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:0fcfd642ec1fe3fb3b9d45a3325811e31d0ed7e9d78d9dc9b4c241c5330a3fd6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7497194 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34822fba9b35aef16f88af40d3ce0a8bc602abdf47b7b28693f1a1e152e4b026`

```dockerfile
```

-	Layers:
	-	`sha256:c229a421def7425a7e30877702ace97054545ad89af73328d44c844eba358223`  
		Last Modified: Fri, 10 Oct 2025 00:36:55 GMT  
		Size: 7.5 MB (7482966 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e18f62575903df59fe3055f658f6e630fc7561dd81cbb3ab5b0f1db4d0fbdbda`  
		Last Modified: Fri, 10 Oct 2025 00:36:56 GMT  
		Size: 14.2 KB (14228 bytes)  
		MIME: application/vnd.in-toto+json
