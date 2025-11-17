## `clojure:temurin-11-tools-deps-bullseye-slim`

```console
$ docker pull clojure@sha256:bb86c86c6760dec9d252c976a53e585ecee1dde777795413132dd0d463672a46
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-tools-deps-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:60e52ed07aaa2d1e5997b95ae75b37b7d41743341280b8b1b4214b04df1e8c8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.4 MB (234377846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7597b736f99fb126e9b527fba18ed7c66058426f9449b09635b17a6298dde38b`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1762202650'
# Fri, 14 Nov 2025 00:30:21 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 14 Nov 2025 00:30:21 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 14 Nov 2025 00:30:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 14 Nov 2025 00:30:21 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 14 Nov 2025 00:51:31 GMT
WORKDIR /tmp
# Fri, 14 Nov 2025 00:51:48 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 14 Nov 2025 00:51:48 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 14 Nov 2025 00:51:48 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:cf5f39ef3fca9730ed04aee5f10040ea152a9793dec0d626f4205eeac5ec3fc0`  
		Last Modified: Tue, 04 Nov 2025 00:13:10 GMT  
		Size: 30.3 MB (30258596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ed3738b87fc4228a7660562fba645d8af058e8adbe26077170065844ea6f192`  
		Last Modified: Fri, 14 Nov 2025 03:44:54 GMT  
		Size: 145.0 MB (144966598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af88cb7e6c76411394c90c24e447d634ed46733b5e698aa81281f6d3d66973de`  
		Last Modified: Fri, 14 Nov 2025 00:52:26 GMT  
		Size: 59.2 MB (59152006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c250ac13f0fd32f32e83e3f019bf4dae6060f1ac65235aedfc9ffed0255c92e3`  
		Last Modified: Fri, 14 Nov 2025 00:52:21 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:41c2f10f19547f0c65fd49c1826652554b625e6276535f6115085a682d58178f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5341674 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6217468f0334d902bca528d534275020de07730cb8c228f527ad78d82d1a464`

```dockerfile
```

-	Layers:
	-	`sha256:f4decca49f329f4c83d239cd6a0df8fb5958d7d1e614472feb1567073af3f03c`  
		Last Modified: Fri, 14 Nov 2025 01:35:48 GMT  
		Size: 5.3 MB (5328208 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e6beb190f7ce570724ff1d20f48ea251dd2c6229eff5bf58ec2c0434e221fcc1`  
		Last Modified: Fri, 14 Nov 2025 01:35:48 GMT  
		Size: 13.5 KB (13466 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:cede0932ebb6e943942eedf52027bc3cb2704ebf0b8bd43fb5d1aafc73474647
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.8 MB (229768453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b77090496ff6067800e4bc375d6324696719aa3299a3bd02494312d6614f688f`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1762202650'
# Fri, 14 Nov 2025 00:53:44 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 14 Nov 2025 00:53:44 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 14 Nov 2025 00:53:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 14 Nov 2025 00:53:44 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 14 Nov 2025 00:53:44 GMT
WORKDIR /tmp
# Fri, 14 Nov 2025 00:53:58 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 14 Nov 2025 00:53:58 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 14 Nov 2025 00:53:58 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:241077dc995c26590e89ca59e622bf97509f2613a9e84e3e745225e4259eb511`  
		Last Modified: Tue, 04 Nov 2025 00:13:03 GMT  
		Size: 28.7 MB (28748552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0805bed4a25ea891a0b10f7855a57a3d448f689bc3ef18dd34207a8be52e3de`  
		Last Modified: Mon, 17 Nov 2025 16:39:55 GMT  
		Size: 141.7 MB (141731559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44e256fd8fc18702b76669c75f18685dbd2c845567dcaf8c8e0a729c836f72f6`  
		Last Modified: Fri, 14 Nov 2025 00:54:34 GMT  
		Size: 59.3 MB (59287694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70b1863b4af083c05f79e18e6f4574fc7846662e5f1b6af46523d612169a090e`  
		Last Modified: Fri, 14 Nov 2025 00:54:27 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:88efe26eee68c0227307d7814835eef331a83bd19df1e0307103e551f7ca45f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5348943 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c494ee38b913412d2b44fba009ad9b44af8e4f374248f5e651d9017987589974`

```dockerfile
```

-	Layers:
	-	`sha256:6495b7c2d2ef452dd249f8f91ba4e1843a008984ed9450d8348563d64ad9d33c`  
		Last Modified: Fri, 14 Nov 2025 01:35:54 GMT  
		Size: 5.3 MB (5334558 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5ccf3f0d2d071455e2d054ebb2678726de2a543cae1c888f48787bd59874edc6`  
		Last Modified: Fri, 14 Nov 2025 01:35:55 GMT  
		Size: 14.4 KB (14385 bytes)  
		MIME: application/vnd.in-toto+json
