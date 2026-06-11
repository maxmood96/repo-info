## `clojure:temurin-11-tools-deps-bullseye`

```console
$ docker pull clojure@sha256:b4bf070615f1ef6cacc848ce03f2e0bdd2a0df2a5910ca51e9c520dfdedca5bb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-tools-deps-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:a98c6bf4f401d53287dce373558ffa304bda40b0621fb96e953f7942baec1275
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.2 MB (266170191 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:363b81b4ba6e6adf42efe4e1a61dbb5534787fa5d354b973e17cfbc247af3a45`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1781049600'
# Thu, 11 Jun 2026 01:18:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Jun 2026 01:18:03 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 11 Jun 2026 01:18:03 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jun 2026 01:18:03 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Thu, 11 Jun 2026 01:18:03 GMT
WORKDIR /tmp
# Thu, 11 Jun 2026 01:18:17 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 11 Jun 2026 01:18:17 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 11 Jun 2026 01:18:17 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:af48a3e7696e07f88a02f9674e541901b65eadb5cf0f62e566b1d895099a1e9e`  
		Last Modified: Wed, 10 Jun 2026 23:40:09 GMT  
		Size: 53.8 MB (53771769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd8e66cf1b6f189b9e522216f794b94603aa358827e01f35cf7dbf9299037d60`  
		Last Modified: Thu, 11 Jun 2026 01:18:42 GMT  
		Size: 145.9 MB (145886263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5b6356a3580218c1a753a52a5eb81989723bf1ca604c79d8f31c2d14f6fb1c1`  
		Last Modified: Thu, 11 Jun 2026 01:18:40 GMT  
		Size: 66.5 MB (66511514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e3ec78ca260cba1d4e3aff23ee7506319a65d2e7c0eca55f9129c8cdf84b969`  
		Last Modified: Thu, 11 Jun 2026 01:18:38 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:19de042316990e60e1d3cbaddffc7b627bf3ffa3349c46b863183629e97ce57f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7439328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4af7c4b5974d1a258f805a7424655ff4493d902329b9256e0b3eb503c42636a4`

```dockerfile
```

-	Layers:
	-	`sha256:96557a7c7f7d002324de8393bb0d1aa9a467a211ba315017d8e41d4354deea41`  
		Last Modified: Thu, 11 Jun 2026 01:18:38 GMT  
		Size: 7.4 MB (7424965 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d6461f94bb03ba326c5471a7d94c0f740480b5d022e8379746ebf12ef2a12593`  
		Last Modified: Thu, 11 Jun 2026 01:18:37 GMT  
		Size: 14.4 KB (14363 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:1d74078d5866220183f76003bfe150b4dde5a83fb96cc3963790469aef18e6e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.5 MB (261524689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:903cc0db329560be09aaf756e5392e648545fd5c671abaea8c5e4abd764dc246`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1781049600'
# Thu, 11 Jun 2026 01:21:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Jun 2026 01:21:56 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 11 Jun 2026 01:21:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jun 2026 01:21:56 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Thu, 11 Jun 2026 01:21:56 GMT
WORKDIR /tmp
# Thu, 11 Jun 2026 01:22:09 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 11 Jun 2026 01:22:10 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 11 Jun 2026 01:22:10 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:7c21e59e753cb91625909251110d6e4cc4a5411b4b7b37f74a62e56b927b7f1e`  
		Last Modified: Wed, 10 Jun 2026 23:39:58 GMT  
		Size: 52.3 MB (52264114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:245303d6ed9e6619ebd4ad5485aa2b12a85a7dd8b2f5c7cfb6a780b6392241bd`  
		Last Modified: Thu, 11 Jun 2026 01:22:33 GMT  
		Size: 142.6 MB (142582228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:848ff18df3b1b587aad4dd6acef0a1b1edd1d2c9c4a38c545504d0353385c512`  
		Last Modified: Thu, 11 Jun 2026 01:22:32 GMT  
		Size: 66.7 MB (66677703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4394f7b5b41af511c96d7e0818de54c9dd4b8984c01729583c81961c5211d5b1`  
		Last Modified: Thu, 11 Jun 2026 01:22:28 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:e7b52d3597e04f848bccce447d826ec5c89390655ea320ce6d035efa9b370c58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7445162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03e8468bca78bbff7b92182974724d535ffbba23ca1d0a3df63a78f35585cc16`

```dockerfile
```

-	Layers:
	-	`sha256:aa34ba0ad0b2c379fdfd48b3aefbb885ba7d15f5212c9eaa8a43239ec2a1621c`  
		Last Modified: Thu, 11 Jun 2026 01:22:29 GMT  
		Size: 7.4 MB (7430682 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b7eb4d2d07042780d1023af489d8e98c5b78bed69efde9046a4a0aec7f010267`  
		Last Modified: Thu, 11 Jun 2026 01:22:28 GMT  
		Size: 14.5 KB (14480 bytes)  
		MIME: application/vnd.in-toto+json
