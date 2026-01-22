## `clojure:temurin-8-tools-deps-bullseye-slim`

```console
$ docker pull clojure@sha256:1521575e1d57497ef58c481d1d910371d0491bf209eda0c10576a0ccc00398c5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:e4a654b8ba24d7ffd857d13e3887d2a61d041da1f20f08385890ed0ec016e324
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.1 MB (144142333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce28136873b183ea747e4a62a11d4f87dbda1a68b9b0fecf725bd056d155039f`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1768176000'
# Fri, 16 Jan 2026 01:45:06 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Jan 2026 01:45:06 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 16 Jan 2026 01:45:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jan 2026 01:45:06 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Fri, 16 Jan 2026 01:45:06 GMT
WORKDIR /tmp
# Fri, 16 Jan 2026 01:45:20 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 16 Jan 2026 01:45:20 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 16 Jan 2026 01:45:20 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:bd1b97a95a10ded4767bfcdbb3d042b961d107d141121fdbb255239f0ca115f4`  
		Last Modified: Tue, 13 Jan 2026 00:42:30 GMT  
		Size: 30.3 MB (30258497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b54dfcc3410864602f4a737b5adbea81b47071a00ff6720edd20fedbcfa8a4e7`  
		Last Modified: Fri, 16 Jan 2026 01:45:35 GMT  
		Size: 54.7 MB (54733367 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74eda9e3530ce8ab794452d9da80d0450b6220e109f316e3ecc34768208a94b8`  
		Last Modified: Fri, 16 Jan 2026 01:45:35 GMT  
		Size: 59.1 MB (59149826 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fcc6973f3867fbc2b42ca0b277d495ed5a7d6ebae286a172b87834e1c0ef04e`  
		Last Modified: Fri, 16 Jan 2026 01:45:33 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:29f0f79145b197d76e1344e46fb84c55078ed24163a11fdca5bd485d4ce8df5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5443924 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:967ebf302c01dcdcdb7399c13a12b36f9d9247d43c29379b4c7d60eeaf755d1a`

```dockerfile
```

-	Layers:
	-	`sha256:f68c4e1b3a0a4bb7d6c9413a606cdd838bd3a4ce3fef19c812956cf4bc7f3299`  
		Last Modified: Fri, 16 Jan 2026 01:45:33 GMT  
		Size: 5.4 MB (5429677 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c7de1100e018db46774283723154183e9006253b9f4a5e8ac3d8017beb61bf07`  
		Last Modified: Fri, 16 Jan 2026 04:52:32 GMT  
		Size: 14.2 KB (14247 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:61ea48fe688f3ada6752b26e26835ab54263a5e0601364db39d7dbd8903f72d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.8 MB (141848034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1caa22b2fbbf4f3576b38fc427d04e4ffc6b871fcc678eb5c26f669bac44c44e`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1768176000'
# Fri, 16 Jan 2026 01:43:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Jan 2026 01:43:57 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 16 Jan 2026 01:43:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jan 2026 01:43:57 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Fri, 16 Jan 2026 01:43:57 GMT
WORKDIR /tmp
# Fri, 16 Jan 2026 01:48:02 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 16 Jan 2026 01:48:02 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 16 Jan 2026 01:48:02 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:7781088accb552d6473ed64f4649a64684d928b7cfad973d13e5c50942bf7a5b`  
		Last Modified: Tue, 13 Jan 2026 00:41:51 GMT  
		Size: 28.7 MB (28748518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72cf421d734f5d2ef3b9813b0ff589dc86cda4fca42b74fb669effd6ba0c978f`  
		Last Modified: Fri, 16 Jan 2026 01:47:05 GMT  
		Size: 53.8 MB (53815013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c852316cd18cba75c148373e925fcc369fd193f7fc66b535fccb1ee51a3a24e`  
		Last Modified: Fri, 16 Jan 2026 01:48:18 GMT  
		Size: 59.3 MB (59283856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3f3742c3f817b6327fb737d0a954f4f75029212afc5fe3351e87414b3de921b`  
		Last Modified: Fri, 16 Jan 2026 01:48:16 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:4cbd50b8d12dde6b150f12b0cce5842d5750cd0ba97044926d9ad2f4162f725a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5450473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b27d10f9fada93d4325a87bd58072e5141f110a14fd83ed18436c439ff13cf0e`

```dockerfile
```

-	Layers:
	-	`sha256:0102bf4e3eeda18999952eaaa124cc223c98b4b8b9e754f3220353f2bc338c0d`  
		Last Modified: Fri, 16 Jan 2026 01:48:16 GMT  
		Size: 5.4 MB (5436107 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4692829d38340cee0334ed150dcf265ad7aef32b486718108bc32c3cd6c293f3`  
		Last Modified: Fri, 16 Jan 2026 01:48:16 GMT  
		Size: 14.4 KB (14366 bytes)  
		MIME: application/vnd.in-toto+json
