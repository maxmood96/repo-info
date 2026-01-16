## `clojure:temurin-11-bullseye-slim`

```console
$ docker pull clojure@sha256:60ff18fa21de17a99d27d0261c7d46b9370fea5a99e0f386355017104a97f48f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:3eead52494c611bcd0e8c677e4b1525a7554a45e8dce00cac7ad9349e70c90a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.4 MB (234375580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02cf541a4e5f187f4b0aa13b3b328df3047d8a1571bb62fc2f72c272b2cdf318`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1768176000'
# Tue, 13 Jan 2026 03:24:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 Jan 2026 03:24:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 Jan 2026 03:24:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 03:24:36 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Tue, 13 Jan 2026 03:24:36 GMT
WORKDIR /tmp
# Tue, 13 Jan 2026 03:28:31 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 13 Jan 2026 03:28:32 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 13 Jan 2026 03:28:32 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:bd1b97a95a10ded4767bfcdbb3d042b961d107d141121fdbb255239f0ca115f4`  
		Last Modified: Tue, 13 Jan 2026 00:42:30 GMT  
		Size: 30.3 MB (30258497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3f17022b9ead5c10b4f6402516879a4a51d4d5d60301e8e7c19b27c5076046f`  
		Last Modified: Tue, 13 Jan 2026 03:25:33 GMT  
		Size: 145.0 MB (144966609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab6df49a51377634e1c6d133357309d42c955b9fa0955d60a61f7397e9a14c55`  
		Last Modified: Tue, 13 Jan 2026 03:28:48 GMT  
		Size: 59.1 MB (59149831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6330ca8a319cda54af400489e87d384eda33dc7825506cd98e65e054a4a4537`  
		Last Modified: Tue, 13 Jan 2026 03:28:54 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:41019fd8ab19b110eb514942f871280e308ee5f0a6458a306f3c67d748232f7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5341674 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4afd45e57023804cff2034ad63499d932fe2f2abf6200f4c70a26b888b02b17`

```dockerfile
```

-	Layers:
	-	`sha256:9c5fc670a1f3a60b532ed6554cd48ac2f2a16e796b0aeb54626696dceaefb87f`  
		Last Modified: Tue, 13 Jan 2026 07:36:57 GMT  
		Size: 5.3 MB (5328208 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1e498f92c5813a015f589f8fd8ce3b968bb19a47c98a100104b50c15abe167a5`  
		Last Modified: Tue, 13 Jan 2026 07:36:57 GMT  
		Size: 13.5 KB (13466 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:1e9fda5f44b279272a5b2d413fcb3a237b4902b66b2cfe5e3df041f7341b1ec8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.8 MB (229764430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c65dbdae3b910447ad328cb93a1ca49463657bf9378bad10dd8a1bbd13bd2cac`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1768176000'
# Tue, 13 Jan 2026 02:32:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 Jan 2026 02:32:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 Jan 2026 02:32:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 02:32:36 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Tue, 13 Jan 2026 03:32:13 GMT
WORKDIR /tmp
# Tue, 13 Jan 2026 03:32:27 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 13 Jan 2026 03:32:27 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 13 Jan 2026 03:32:27 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:7781088accb552d6473ed64f4649a64684d928b7cfad973d13e5c50942bf7a5b`  
		Last Modified: Tue, 13 Jan 2026 00:41:59 GMT  
		Size: 28.7 MB (28748518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1510e970ac0ccbb2caa1a380c52e46c23c443b37bdc304200129ebb532bb400c`  
		Last Modified: Tue, 13 Jan 2026 09:53:54 GMT  
		Size: 141.7 MB (141731578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2e46815bf7341c15e4c0b622f31655a03646e41e02d8aa726b64d75d2af1963`  
		Last Modified: Tue, 13 Jan 2026 03:32:55 GMT  
		Size: 59.3 MB (59283690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2834744cb3be94c868b6f01484203303f979ceae460a019a70fd8cf842be61e3`  
		Last Modified: Tue, 13 Jan 2026 03:32:58 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:a128ae3a2a6dcf59fbcfd629122aa6715934c95ad5e2fe11803fde171572dcd8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5348142 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4b1fe85e090f9d294165ed4c160be193257fc4c0cee3254ec76562b3792f6e8`

```dockerfile
```

-	Layers:
	-	`sha256:3f8bd0a5fb278a2d67fdefac2dfcdbfde683499d781b2408994c535ff48ed6f9`  
		Last Modified: Tue, 13 Jan 2026 07:37:05 GMT  
		Size: 5.3 MB (5334558 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a0ac381d815ed009b17c6cff3bf1f6fe6550fe7f744410413c0e8fd22d2e0b35`  
		Last Modified: Tue, 13 Jan 2026 07:37:05 GMT  
		Size: 13.6 KB (13584 bytes)  
		MIME: application/vnd.in-toto+json
