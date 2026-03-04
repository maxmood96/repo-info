## `clojure:temurin-17-tools-deps-bullseye`

```console
$ docker pull clojure@sha256:a05add87e4f529f6b3fab503efa6e4102488d15ed95c928ee87a5c67654dd8d3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-tools-deps-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:9cb5d7548be6ee18324b3d6a0ab3c7b5abfcc2681e886095c33003a2554569e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.0 MB (268973755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d453dec696f7749f8c97010d4794df9ea545322172160b24a1f8de33a071613a`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1771804800'
# Wed, 04 Mar 2026 17:50:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 04 Mar 2026 17:50:12 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 04 Mar 2026 17:50:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Mar 2026 17:50:12 GMT
ENV CLOJURE_VERSION=1.12.4.1612
# Wed, 04 Mar 2026 17:50:12 GMT
WORKDIR /tmp
# Wed, 04 Mar 2026 17:50:26 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "21d16fbce3e546c4f0163c78aba0eb0293993c7fa1aba77d089fdbfa445e38a2 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 04 Mar 2026 17:50:26 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 04 Mar 2026 17:50:26 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 04 Mar 2026 17:50:26 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 04 Mar 2026 17:50:26 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:fd834ead99fe4ea0884686321217c38494a7a0c7327e2a5ed98d978011de7ddb`  
		Last Modified: Tue, 24 Feb 2026 18:43:07 GMT  
		Size: 53.8 MB (53756434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:958b3a08b9192579c65ea6d090323403c7344a2f7d01221a07d5dce5d21a1efa`  
		Last Modified: Wed, 04 Mar 2026 17:50:45 GMT  
		Size: 145.6 MB (145628716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:766ef7de915e95f96b887c43ab7fc373d85bac0d3dea59897635388f78a87c59`  
		Last Modified: Wed, 04 Mar 2026 17:50:48 GMT  
		Size: 69.6 MB (69587563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2299a1c8ac09f7db4d603264ae41030ff00d50d42815b3145901b7ca8158019f`  
		Last Modified: Wed, 04 Mar 2026 17:50:45 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a80f5072358dd1f3195e2fe673fa1fab8700f45ac00c2d11367ac40d3fdfdbc`  
		Last Modified: Wed, 04 Mar 2026 17:50:45 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:c3ae361d15fa9936533b5064c95c78db6f7ca9dd425f6f717ca16d1a73e06c9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7425055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b32ae3d0ebd02750e9b01f95c0bf1b297ff68471ad6af2118473d83759146d4`

```dockerfile
```

-	Layers:
	-	`sha256:a3539fd1dcab9ccf94dc5088771835d7314076ee83683aaa061e8f15be47163a`  
		Last Modified: Wed, 04 Mar 2026 17:50:45 GMT  
		Size: 7.4 MB (7409277 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:267cf003cacedee00372858a8569e85ea943742e5f05e4e5e77ac782a17d957c`  
		Last Modified: Wed, 04 Mar 2026 17:50:45 GMT  
		Size: 15.8 KB (15778 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:2c9fc616d13e9846a7c1a64e6d93c1755981682f93702930ac7fbc6fc3991a9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.4 MB (266424216 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf327c8d1f6e539a61820c9d321e9a3a13d474b8b69f2716e42d0ba0f7e0843e`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1771804800'
# Wed, 04 Mar 2026 17:49:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 04 Mar 2026 17:49:46 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 04 Mar 2026 17:49:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Mar 2026 17:49:46 GMT
ENV CLOJURE_VERSION=1.12.4.1612
# Wed, 04 Mar 2026 17:49:46 GMT
WORKDIR /tmp
# Wed, 04 Mar 2026 17:50:00 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "21d16fbce3e546c4f0163c78aba0eb0293993c7fa1aba77d089fdbfa445e38a2 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 04 Mar 2026 17:50:00 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 04 Mar 2026 17:50:00 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 04 Mar 2026 17:50:00 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 04 Mar 2026 17:50:00 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:0509053f2cf8072309184287dd2fd397e589dc5db17a1ddc469001be80ea07a3`  
		Last Modified: Tue, 24 Feb 2026 18:42:38 GMT  
		Size: 52.3 MB (52258392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ada62ba62fb9f123320f63e92ebd3322c984d14254b9b23455210d1800d3da9`  
		Last Modified: Wed, 04 Mar 2026 17:50:23 GMT  
		Size: 144.4 MB (144436183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e05ad77e1d1274c89db606f11d5982be482a6dafe5ec943ffec20f6ed28b723c`  
		Last Modified: Wed, 04 Mar 2026 17:50:22 GMT  
		Size: 69.7 MB (69728599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce491bdcc7fe179b3a335aaa2fa493e45790722364ae8d75db57d0af9a7bbfcc`  
		Last Modified: Wed, 04 Mar 2026 17:50:19 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c6169e02a2f88b0d35e85178306146ea7857b58a630e101199a225d982bb6e3`  
		Last Modified: Wed, 04 Mar 2026 17:50:19 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:f14c89a178008dfa85a402120cc1f3f40021107838c171d3c25e889dca7759e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7430272 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75fc6d9929ea96b951d5e037c9d54e1c79b6d104e72623a88bd59efc730a6ffd`

```dockerfile
```

-	Layers:
	-	`sha256:0518442f96cf1661fdfe417222fe782390bc455262a0460db3ff15c454289445`  
		Last Modified: Wed, 04 Mar 2026 17:50:19 GMT  
		Size: 7.4 MB (7414376 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:802090ef990a2b709e5d84233bb4c53638f95311e595617d8cc8dafb40fe5410`  
		Last Modified: Wed, 04 Mar 2026 17:50:19 GMT  
		Size: 15.9 KB (15896 bytes)  
		MIME: application/vnd.in-toto+json
