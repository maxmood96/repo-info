## `clojure:temurin-26-tools-deps-1.12.5.1638-bullseye-slim`

```console
$ docker pull clojure@sha256:9b72c540a8fe6c192d9f78efb725476bf71801f317c4195f17688adcf11f627e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-26-tools-deps-1.12.5.1638-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:fb06f877e0beaff5b0b380a828e02c5966d36bdba8664ddecf81b20464ee2691
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.9 MB (183929857 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a700dcbee2f615c53298d96ec86558b80f273c05534e7d74a31123624989c4b3`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1777939200'
# Thu, 14 May 2026 23:37:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 14 May 2026 23:37:01 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 14 May 2026 23:37:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 14 May 2026 23:37:01 GMT
ENV CLOJURE_VERSION=1.12.5.1638
# Thu, 14 May 2026 23:37:01 GMT
WORKDIR /tmp
# Thu, 14 May 2026 23:37:14 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "bccfca8c437514786f0827a11195b89b833357b2a668091f4321b451b2e36df5 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 14 May 2026 23:37:14 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 14 May 2026 23:37:14 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 14 May 2026 23:37:14 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 14 May 2026 23:37:14 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:77e30ef52aeb52d8466baf0f50b54ed2fc0b421f44c49e5bf93682b27110f4d3`  
		Last Modified: Fri, 08 May 2026 18:22:59 GMT  
		Size: 30.3 MB (30257958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8626a4b2147ef9bee220cedca3e64a2228de605e71bd773731c881c68ec68f1`  
		Last Modified: Thu, 14 May 2026 23:37:36 GMT  
		Size: 94.5 MB (94455681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c6102e27d0a29f17aef9359a355841fef85d234a4b75fd15ae4215d800dbc6f`  
		Last Modified: Thu, 14 May 2026 23:37:34 GMT  
		Size: 59.2 MB (59215174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d7ccb90fc7aed01ad5b005ae9a7413d13b0c07c96e3809d92136e904948b13d`  
		Last Modified: Thu, 14 May 2026 23:37:32 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:823a8f5a6f6dd64f0ee2461271e66943edde11250979bcc2c09de92adac72554`  
		Last Modified: Thu, 14 May 2026 23:37:32 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-tools-deps-1.12.5.1638-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:5883a8eb224fdb9cdf237d8bf35c45955d567104d839f46edae5e3f3cb12cd5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5301384 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75382c28954a4e358a4bfa90338098a5e1da6f181b5e4365349ee6f2a3322c91`

```dockerfile
```

-	Layers:
	-	`sha256:2a36bfc07e37f218d6d847f43f63ca6f96ff32c3c31ea7469afac5d7619d3aa2`  
		Last Modified: Thu, 14 May 2026 23:37:32 GMT  
		Size: 5.3 MB (5285555 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:97c9e2278dbab13cfcda7bb060770441437eecd07b649501ea3e511d1d2ac750`  
		Last Modified: Thu, 14 May 2026 23:37:32 GMT  
		Size: 15.8 KB (15829 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-tools-deps-1.12.5.1638-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:ef13af383262ff69841394e5b4baadcc4be93d631a56750031f869420fc97406
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.5 MB (181496923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f551e357364af6c581ab85f7d4d45fbf31f209dc4e908c92a5d9f6c2d014f489`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1777939200'
# Thu, 14 May 2026 23:37:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 14 May 2026 23:37:05 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 14 May 2026 23:37:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 14 May 2026 23:37:05 GMT
ENV CLOJURE_VERSION=1.12.5.1638
# Thu, 14 May 2026 23:37:05 GMT
WORKDIR /tmp
# Thu, 14 May 2026 23:37:19 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "bccfca8c437514786f0827a11195b89b833357b2a668091f4321b451b2e36df5 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 14 May 2026 23:37:19 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 14 May 2026 23:37:19 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 14 May 2026 23:37:19 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 14 May 2026 23:37:19 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:ab0f13d792ff9100407906fb422a0b62a8b437abde4c245e03f0366814be9aae`  
		Last Modified: Fri, 08 May 2026 18:25:06 GMT  
		Size: 28.7 MB (28742591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcf1e5bc0e25783c9c6a9c154741d0bfafc184f6078d94d14cba433b054ab282`  
		Last Modified: Thu, 14 May 2026 23:37:41 GMT  
		Size: 93.4 MB (93395168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2846d8295a8446985603db3bfc9eb14a6e33beda0e598b55a5a9e79f62f88cb`  
		Last Modified: Thu, 14 May 2026 23:37:40 GMT  
		Size: 59.4 MB (59358122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36a227a7931a6527e1657ee8a9d0b0ce7ce9f804cdea46fa786acbc4acc7fe19`  
		Last Modified: Thu, 14 May 2026 23:37:36 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f02aaa5f8dc5c817930a0460d1508b46e1bdc1e88530f4ccf5e04ba5f399e002`  
		Last Modified: Thu, 14 May 2026 23:37:36 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-tools-deps-1.12.5.1638-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:a9000e9f552425930130496520da8dd50e336a8e56e115199c4b1d718792594e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5307231 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4bfdce5d8b2e0bc68342cb7af5c9b0aad30c6246dde9e4c3dfbd03479c4e75f`

```dockerfile
```

-	Layers:
	-	`sha256:1d1a9bbe34c753d11f44616c2e376ba7ee60910cb8cea96377736dc35894b110`  
		Last Modified: Thu, 14 May 2026 23:37:37 GMT  
		Size: 5.3 MB (5291284 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:57cc280dfc9b3dab1560d812032d893f2d61e55824fa2dee981121296bdf0bf8`  
		Last Modified: Thu, 14 May 2026 23:37:37 GMT  
		Size: 15.9 KB (15947 bytes)  
		MIME: application/vnd.in-toto+json
