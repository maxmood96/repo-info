## `clojure:temurin-8-bookworm`

```console
$ docker pull clojure@sha256:235abc09d8032916649a4df9264c347b5574889d12c07744f5dda096f95b7c93
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `clojure:temurin-8-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:4483568b33bdb2e989e77e67b0591eee919089c2efe0b4044b49033ccdd1edd8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.8 MB (181826734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a9a24b59149f06e8c3802288d2f1634614456aa80922b9dbeefedefa5a9a2d0`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1781049600'
# Fri, 19 Jun 2026 02:14:32 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 19 Jun 2026 02:14:32 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 19 Jun 2026 02:14:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 19 Jun 2026 02:14:32 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Fri, 19 Jun 2026 02:14:32 GMT
WORKDIR /tmp
# Fri, 19 Jun 2026 02:14:46 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 19 Jun 2026 02:14:46 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 19 Jun 2026 02:14:46 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:01cedcff86f879d042805360ecba268802bec3d8201484ff3ec54f4250a2d3b7`  
		Last Modified: Wed, 10 Jun 2026 23:39:39 GMT  
		Size: 48.5 MB (48502042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa57e6ad60d5b1715adcde0d959fe2451e996ddc44ac7c770b0e5a0afa1b0bdd`  
		Last Modified: Fri, 19 Jun 2026 02:15:05 GMT  
		Size: 55.2 MB (55198685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ddc48521fdd79ea8d3677ecc51940a78ff4377c871df7d92fc4b015fb98c861`  
		Last Modified: Fri, 19 Jun 2026 02:15:05 GMT  
		Size: 78.1 MB (78125362 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e8f0aae0bef250229d5e7bf5c6535c39247ef3e012db776683514bf9cb853a0`  
		Last Modified: Fri, 19 Jun 2026 02:15:02 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:c0240ca36e23d4598f0da84e2da62e089d357c1c07e985052843d92fb8ed0ca6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7510842 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5aac21fefd7a220ef1fc6bc4073edc3d7a95c2ad54906f03841351826849ceae`

```dockerfile
```

-	Layers:
	-	`sha256:f86ed268bee4bd5fc101f360fe8df08614b653f4edb298808a0578fd245ebd83`  
		Last Modified: Fri, 19 Jun 2026 02:15:03 GMT  
		Size: 7.5 MB (7496494 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f4bd77aaea0cd37d128a1935621ac7616f1bf99df37c6f4487f27c31a995e4ad`  
		Last Modified: Fri, 19 Jun 2026 02:15:02 GMT  
		Size: 14.3 KB (14348 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:783ff5180eb1c4eb8fc002e31a75e7aee7ecc938a9e2c4e9493716359a355d50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.8 MB (180791688 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75a9268e7ef13253544b5be0e19cb424c1fb6d4160798333180cd617b6e3164e`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1781049600'
# Fri, 19 Jun 2026 02:14:45 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 19 Jun 2026 02:14:45 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 19 Jun 2026 02:14:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 19 Jun 2026 02:14:45 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Fri, 19 Jun 2026 02:14:45 GMT
WORKDIR /tmp
# Fri, 19 Jun 2026 02:14:59 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 19 Jun 2026 02:15:00 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 19 Jun 2026 02:15:00 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:c847f328095fb083f4a22895b90fe4226efa6458ac57362b64b6e5d99da9e4a3`  
		Last Modified: Wed, 10 Jun 2026 23:39:28 GMT  
		Size: 48.4 MB (48389016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3192e2def529202afd2c5ccb59ce6a08c859d8a55e1d64c501002ed119482c3`  
		Last Modified: Fri, 19 Jun 2026 02:15:18 GMT  
		Size: 54.3 MB (54272934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7b4802d6178c5ddea182de5f65e4524d380f16262d5066570f4fb0eda6cb93a`  
		Last Modified: Fri, 19 Jun 2026 02:15:19 GMT  
		Size: 78.1 MB (78129096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7912959e278a8ac896fce6d2eb1a34f6a95d1308277a5bae66cb02653b8ec9d1`  
		Last Modified: Fri, 19 Jun 2026 02:15:16 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:9a1544b8c121deb3ce215dbb7bd5157e5fddae634852760f2c7f455ff7ffc8ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7517423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a9f4e29ef9b6b00423dc30f472d7834af090b6c2f8c576992f500231cacee02`

```dockerfile
```

-	Layers:
	-	`sha256:9adec671f47a743a0dafde08abb8a876fb965c568a28720d3f184280fe27d313`  
		Last Modified: Fri, 19 Jun 2026 02:15:16 GMT  
		Size: 7.5 MB (7502957 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ca671caf25b1ac81979df5d90d2c0f6821aa09c422e2cf7a2f1c8eabc6ea6578`  
		Last Modified: Fri, 19 Jun 2026 02:15:16 GMT  
		Size: 14.5 KB (14466 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-bookworm` - linux; ppc64le

```console
$ docker pull clojure@sha256:7db0244ceea46763b02d82e87f3b88278e21fe8e20b295e1bdf8427ba7044307
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **189.0 MB (188974994 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:132432af58458c0fb32d76989077d1c233ac6dafe764ab5e4e0e459852cf83be`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1781049600'
# Fri, 19 Jun 2026 02:20:44 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 19 Jun 2026 02:20:44 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 19 Jun 2026 02:20:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 19 Jun 2026 02:20:44 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Fri, 19 Jun 2026 02:20:44 GMT
WORKDIR /tmp
# Fri, 19 Jun 2026 02:21:25 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 19 Jun 2026 02:21:26 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 19 Jun 2026 02:21:26 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:88b94a58fac236a778527a3293ccd0ff4d309bff0bf314017ea5af603908fa2e`  
		Last Modified: Thu, 11 Jun 2026 00:21:34 GMT  
		Size: 52.3 MB (52346670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:844528f776a6b2e898eb00a455f654e035ad1f6524a5c71daefb37c7ef673cc4`  
		Last Modified: Fri, 19 Jun 2026 02:22:08 GMT  
		Size: 52.7 MB (52669121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed3fc1e82c3b98ac6a37b46bbf0b33490297e5af08a019338c283c00a0446f31`  
		Last Modified: Fri, 19 Jun 2026 02:22:09 GMT  
		Size: 84.0 MB (83958556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:690bc2be7222ec88cf8eb16118cbdbdcc0449831131a81f312240197575ac3c3`  
		Last Modified: Fri, 19 Jun 2026 02:22:06 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:448513c91f3e1217f219819ee1013d1e805809f98e6f892b0a7bd2618442ba01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7516701 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eecae55ee78ecb28f9b8144abcf81a7a7041f618a303197d1e41e69b41cf93c6`

```dockerfile
```

-	Layers:
	-	`sha256:dba6d646424f3e066ae99fe70205d4d187963ad3d96c41265b13ddb29befa75a`  
		Last Modified: Fri, 19 Jun 2026 02:22:06 GMT  
		Size: 7.5 MB (7502305 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:83272676da63f6a6a966208660d6e33491ecfe7ef74ec16434b7d2b063ab6801`  
		Last Modified: Fri, 19 Jun 2026 02:22:05 GMT  
		Size: 14.4 KB (14396 bytes)  
		MIME: application/vnd.in-toto+json
