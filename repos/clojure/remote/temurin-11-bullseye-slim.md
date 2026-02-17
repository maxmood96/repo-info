## `clojure:temurin-11-bullseye-slim`

```console
$ docker pull clojure@sha256:5f8878f615bf997c2b98367880dd7a266638279dad55e028c02f73cbe5b2a41b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:a3f0fbf141ca4d7f82fac2ef60ea5b1fe751b47e8993a870b1e2f2dfbcc1bce0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.2 MB (235202212 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7ee3eb19c94d53099bfa480ce47c23f88c0c51e238380f5e1e27466a362664a`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1769990400'
# Tue, 17 Feb 2026 21:24:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Feb 2026 21:24:57 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Feb 2026 21:24:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 21:24:57 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 17 Feb 2026 21:42:08 GMT
WORKDIR /tmp
# Tue, 17 Feb 2026 21:42:22 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 17 Feb 2026 21:42:22 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 17 Feb 2026 21:42:22 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:1c3e0f92551cc087b68faa686aead2fc80d99c54c34e9e72a0db197b668ac6be`  
		Last Modified: Tue, 03 Feb 2026 01:14:04 GMT  
		Size: 30.3 MB (30258284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1186ff483f55b35315a261fe0d973cbd4e2b47d43cd925f7254cae1290132c6`  
		Last Modified: Tue, 17 Feb 2026 21:25:51 GMT  
		Size: 145.8 MB (145806706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61417c8f7694247e9d4fadc788ecd39fb63c0cfbede84a15f5993a9be36041b5`  
		Last Modified: Tue, 17 Feb 2026 21:42:37 GMT  
		Size: 59.1 MB (59136575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f19d982c9810ea6d329b8458e711ca35eae610f8ca06ed33f9e261a34a5fd4ac`  
		Last Modified: Tue, 17 Feb 2026 21:42:35 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:c3f2fedd759db5dc5c30defcdb2def9f8e9a50a2e189f69aef828337b7438971
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5343726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f426e8e853e891dd19a93bedbe7114c1e40fb7a4f137a0865a08979bded9470`

```dockerfile
```

-	Layers:
	-	`sha256:2feed49607c194b8e28a59f7a484822c331bcc21ecbef27e736be7a034d27fc1`  
		Last Modified: Tue, 17 Feb 2026 21:42:35 GMT  
		Size: 5.3 MB (5330261 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f6aa504e89e6dacc3dbe051b886594924c04d60964e3f6e855cefc0de4d78820`  
		Last Modified: Tue, 17 Feb 2026 21:42:35 GMT  
		Size: 13.5 KB (13465 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:610895616f6c00f6cda523f5d35daff72253a246af325779a4d34b1ea713ef29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.5 MB (230534666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e888ea5a5b5b2c1222c37222dc1face17411e1bf4e8a288335b40eb620d99b29`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1769990400'
# Tue, 17 Feb 2026 21:42:02 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Feb 2026 21:42:02 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Feb 2026 21:42:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 21:42:02 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 17 Feb 2026 21:42:02 GMT
WORKDIR /tmp
# Tue, 17 Feb 2026 21:42:16 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 17 Feb 2026 21:42:16 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 17 Feb 2026 21:42:16 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:0bab5b9a037a7924cbfa7e0cedabf52dc41fc1e49df102241165282dd277e254`  
		Last Modified: Tue, 03 Feb 2026 01:14:08 GMT  
		Size: 28.7 MB (28744439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:758fd9b856cac4ac4dc7a86e40aeb65cc40c0086112f540b08a0e793e7ea9c07`  
		Last Modified: Tue, 17 Feb 2026 21:42:37 GMT  
		Size: 142.5 MB (142501422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45d6626a77f2fae3a10ae77f965d720c32dbcbad27d74e719a098ce4705339b0`  
		Last Modified: Tue, 17 Feb 2026 21:42:36 GMT  
		Size: 59.3 MB (59288159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adc599f70706a3090c5ebd37dd58aa5df744f5fe4a998ba5e0a27ed13d4ae357`  
		Last Modified: Tue, 17 Feb 2026 21:42:33 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:d27125ed1c76d1ed10e88d7f3b570f5210aa0d4bddf2335248ccdd0d89b6c7ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5350995 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be7b2e86c52f9b1c4d9378c3801ff7b0b910991678a19da9ce165a94916796d1`

```dockerfile
```

-	Layers:
	-	`sha256:a45a8c8fe33f9bca3a40a9b49e9b9104fbaa7070b9114f81d1302bcd4464bd43`  
		Last Modified: Tue, 17 Feb 2026 21:42:34 GMT  
		Size: 5.3 MB (5336611 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4d228e84cc7f27f5727429c9a6736eeeb8658a361b5bfe3794ce1e6fcbd51156`  
		Last Modified: Tue, 17 Feb 2026 21:42:33 GMT  
		Size: 14.4 KB (14384 bytes)  
		MIME: application/vnd.in-toto+json
