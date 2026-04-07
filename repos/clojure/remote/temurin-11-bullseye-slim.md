## `clojure:temurin-11-bullseye-slim`

```console
$ docker pull clojure@sha256:4cb9242e0ba2c740ac34b7e00b5d10dd6c5278261b2899e89fba712edfe9c524
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:01008d2bff4c183a38b84090c8761ffcc4c4b25756c11991c56cb0f4135ea04a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.2 MB (235249364 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09c37a8c2b8fc93341f4b58dc10c8c9a267dba32304f3f25158df446a1596eb3`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1775433600'
# Tue, 07 Apr 2026 02:58:44 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 07 Apr 2026 02:58:44 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 07 Apr 2026 02:58:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 02:58:44 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Tue, 07 Apr 2026 03:13:22 GMT
WORKDIR /tmp
# Tue, 07 Apr 2026 03:14:06 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 07 Apr 2026 03:14:06 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 07 Apr 2026 03:14:06 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:60fb1d5aba60afdf7cbf00cf9bd0c125e0c9c2ef7f454a7a88b456dd51794fab`  
		Last Modified: Tue, 07 Apr 2026 00:11:21 GMT  
		Size: 30.3 MB (30258019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:021150f9fb3c64ec9d05eb82cff69efb46c53664b5fe16cf16e18fde100652a8`  
		Last Modified: Tue, 07 Apr 2026 02:59:28 GMT  
		Size: 145.8 MB (145806958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6b66f09a227a09614bde06c4941b89d9669259cd6471ad692859fb087c151a5`  
		Last Modified: Tue, 07 Apr 2026 03:14:20 GMT  
		Size: 59.2 MB (59183742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e6a772fab287b447a101b444de918d0be6adce7fad8bed45d25fd5c8e8dacef`  
		Last Modified: Tue, 07 Apr 2026 03:14:18 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:38e6f67a7f397408b55f2ef435453940ad19e23c63cd9ca53b844cd0fa37e32c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5353659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98c94c555b9f547be6b8b7dd0abd58fb5d5dec1fea150d0f72393566006c8687`

```dockerfile
```

-	Layers:
	-	`sha256:c0ace879b89c31a6d7fa4736ed2de23165a862068b7a887850ee982877ce0183`  
		Last Modified: Tue, 07 Apr 2026 03:14:18 GMT  
		Size: 5.3 MB (5340194 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c3ab6df723801c6fbb4477192c3ac8f8a39e043b541a0ae5d26403d1414f6cb`  
		Last Modified: Tue, 07 Apr 2026 03:14:18 GMT  
		Size: 13.5 KB (13465 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:fa7fd4004607027097439e05796b25b22199c6ae62f94d8827268a31420f3f1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.6 MB (230569001 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c09c2c18d3fe3f2460da3f45204e945dd302adad6188f844d361d0541bcd2b9`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1775433600'
# Tue, 07 Apr 2026 03:24:32 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 07 Apr 2026 03:24:32 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 07 Apr 2026 03:24:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 03:24:32 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Tue, 07 Apr 2026 03:24:32 GMT
WORKDIR /tmp
# Tue, 07 Apr 2026 03:24:47 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 07 Apr 2026 03:24:47 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 07 Apr 2026 03:24:47 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:44aeebb720693ad47eb3913009383fd4ae7e8c24a3e1abb1683ccdac7f879495`  
		Last Modified: Tue, 07 Apr 2026 00:11:03 GMT  
		Size: 28.7 MB (28744688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:174009bf6fae4b344abdb49adcc543be6ec6b2526bbfea7ab2a99ba89e0d97a4`  
		Last Modified: Tue, 07 Apr 2026 03:25:09 GMT  
		Size: 142.5 MB (142500043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04ef6b17c20173f8477e8ce29b5cee3d59b6fb12db512cd9138454e6e41db33e`  
		Last Modified: Tue, 07 Apr 2026 03:25:07 GMT  
		Size: 59.3 MB (59323625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e7df628c213adf8d8702e8c8fe737a2906cffeea3f9fcc17804164cc109d5c0`  
		Last Modified: Tue, 07 Apr 2026 03:25:04 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:2aa44239898975dfb7437bb4e70f756829b69be34eb0575dcce2930c34c1ab95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5360929 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:437d00c687f669fab38c916c82679df26553cc9fbf0a19ed33fe54735d8565e4`

```dockerfile
```

-	Layers:
	-	`sha256:e573126bdd5c2b6a514c864272e20c04d42cb0ad2433e89a293bb460d7883979`  
		Last Modified: Tue, 07 Apr 2026 03:25:05 GMT  
		Size: 5.3 MB (5346544 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a1bbccc59ca976061faeb8e19b8dedf760baf7bbbfd0bd9e77ef6b35977ede18`  
		Last Modified: Tue, 07 Apr 2026 03:25:04 GMT  
		Size: 14.4 KB (14385 bytes)  
		MIME: application/vnd.in-toto+json
