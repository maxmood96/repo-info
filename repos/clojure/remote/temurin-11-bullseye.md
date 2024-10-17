## `clojure:temurin-11-bullseye`

```console
$ docker pull clojure@sha256:6f2ec719625100e327a26bf7f3b21e6f87041f80779c5ca164c675b76b7bd756
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:ec15396f16101c4bc031550b23941877487604cc5ee92608d4b8f75f5f07617b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **270.0 MB (269964713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4afde700276e1fb2add978741a74dfae1f17259dc60253133c2c30e4414011c1`
-	Default Command: `["clj"]`

```dockerfile
# Thu, 03 Oct 2024 17:49:34 GMT
ADD file:603894b180221fc8174e291cd1177a2b9c09a07d1d9ba4d5b5aecdf80ad91fbb in / 
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
	-	`sha256:9439c0e98e5f72dba1ea7cf303c3ca61ff9a91b26911886adb4266e2ad40bb58`  
		Last Modified: Thu, 17 Oct 2024 00:24:16 GMT  
		Size: 55.1 MB (55080611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20b249d71eb4253dc1b0a43d1d1effe7c614c80fa62976933a077c4ceb30394f`  
		Last Modified: Thu, 17 Oct 2024 01:13:46 GMT  
		Size: 145.5 MB (145549876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:febcb6ba90e52cae858603e63a5f332fd16eee445db4c5154d32f350756445a7`  
		Last Modified: Thu, 17 Oct 2024 01:13:45 GMT  
		Size: 69.3 MB (69333583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f13c973af2c4f0fe01cf2b9705a3fe401216023e76453b017e281837370d0d4e`  
		Last Modified: Thu, 17 Oct 2024 01:13:42 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:fd357f234fa9f40498097f0d673a40bfe11c4b05f290a2d8d45960af6f815588
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7224163 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e495f322ed9acbfba447881d4e452676a0d52421926a3e97ca2f712cd760cbe`

```dockerfile
```

-	Layers:
	-	`sha256:db5de7e43fee1a22146391a6cbebd56450302f6413f21b0d6baa01ba6c7f22e4`  
		Last Modified: Thu, 17 Oct 2024 01:13:43 GMT  
		Size: 7.2 MB (7210260 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bad4637d460cfa1982cd2dfe3672d89f608eb804d0b342be3684f8e3e805079f`  
		Last Modified: Thu, 17 Oct 2024 01:13:42 GMT  
		Size: 13.9 KB (13903 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:f26aa53d764d2aa57dfa85c5410dd158ad5155b257c5ad397ada570cc94ca628
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **265.6 MB (265558958 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb6c6e1cff43e0652992b4b19f980e4e8107fd1f80c4d6a3e60f2d4a218d4d0f`
-	Default Command: `["clj"]`

```dockerfile
# Thu, 03 Oct 2024 17:49:34 GMT
ADD file:bfb52ce9788d517977c9e84dad795a6adb46efc0e8eff88853137b783826c104 in / 
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
	-	`sha256:76475c2689e229fac9e8ba4a02e64decb7fd62b2a3e4ad65ba97f8e1a35471f2`  
		Last Modified: Thu, 17 Oct 2024 01:14:55 GMT  
		Size: 53.7 MB (53734895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bda293784e347b2519c90ccae374d1fef0769a110f0539ea381e5d0173cef5f`  
		Last Modified: Thu, 17 Oct 2024 08:05:45 GMT  
		Size: 142.4 MB (142356620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32c05e41003ac86805de7b845a5875e74c40c76671bd8a5c23512babc22e02d5`  
		Last Modified: Thu, 17 Oct 2024 08:09:35 GMT  
		Size: 69.5 MB (69466801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4846c262d2b2b6d62709604ec56bc778b2aceb4a43e1d283e664537b3b30fadc`  
		Last Modified: Thu, 17 Oct 2024 08:09:33 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:2874ce29bd18fcc414421f9cc02d5360b934d62cbef9b10655d033694e2c23ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7229991 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1366e5b9bcf46c796d5a68459a00f82d831abe1e32b346903ccc275b6bbcc357`

```dockerfile
```

-	Layers:
	-	`sha256:a182b0efb885c7e9a9e7a990388086598e2a29d300cefdf521a2cf9af04d068b`  
		Last Modified: Thu, 17 Oct 2024 08:09:34 GMT  
		Size: 7.2 MB (7215982 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bfb3a8772bfc585c9d03e29cdd36f1268bfdb00d6eebda0d404b1d70b8940374`  
		Last Modified: Thu, 17 Oct 2024 08:09:33 GMT  
		Size: 14.0 KB (14009 bytes)  
		MIME: application/vnd.in-toto+json
