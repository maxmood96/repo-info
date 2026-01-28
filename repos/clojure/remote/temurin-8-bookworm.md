## `clojure:temurin-8-bookworm`

```console
$ docker pull clojure@sha256:ebb95be9a04ad31552f5726612e6874be8e529851b0cba97024333e9f8d78c5b
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
$ docker pull clojure@sha256:bc473d2d5940053f0d059c82ff67a79fcda3070155c37b3be4cae394220ad3a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.4 MB (184366077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b773ccc5611479128540967665a5e02c28dbeca87f3ab3076aaeefe4e7ffc6f`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1768176000'
# Wed, 28 Jan 2026 18:02:40 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 28 Jan 2026 18:02:40 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 28 Jan 2026 18:02:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Jan 2026 18:02:40 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Wed, 28 Jan 2026 18:02:40 GMT
WORKDIR /tmp
# Wed, 28 Jan 2026 18:02:55 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 28 Jan 2026 18:02:55 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 28 Jan 2026 18:02:55 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:c1be109a62df95316ceac87ea501079f32e17f36b636865a860841b7db06100c`  
		Last Modified: Tue, 13 Jan 2026 00:41:15 GMT  
		Size: 48.5 MB (48481622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:419068959cc702e3fb4d1a965f731abf5f805d80bf3dcdf1f054259f592de529`  
		Last Modified: Wed, 28 Jan 2026 18:03:13 GMT  
		Size: 54.7 MB (54733356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87b375e764357b16d76c24545090c5dad4d148205850bfd11e7909c1262ac1be`  
		Last Modified: Wed, 28 Jan 2026 18:03:13 GMT  
		Size: 81.2 MB (81150455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f359950b9290c2041a1076e35c49b23ebac216d808d1b0cf639e0d57bfe09315`  
		Last Modified: Wed, 28 Jan 2026 18:03:11 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:1a29743ec2b753defb6b9d3479b624f9f4c0fb46f612ef5bf048917f6f008909
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7511339 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:370a636c8e4adf923e768ff1f3c39975a70ca6b462ef4ee76a73ca61ea60ebe1`

```dockerfile
```

-	Layers:
	-	`sha256:03873efb4332a33ce4770e6dbe54f90e85175f5889672cbc0942d527a5d5d1d7`  
		Last Modified: Wed, 28 Jan 2026 18:03:11 GMT  
		Size: 7.5 MB (7497145 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3b1f60949d496eff1a4ee14f425acc544d3d06aa9adb9a9b8b511e05dcd1803f`  
		Last Modified: Wed, 28 Jan 2026 18:03:10 GMT  
		Size: 14.2 KB (14194 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:c5550004510ce3c3565bfda17b0117d3ff24583e8249cb34d989af37410a11d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.3 MB (183320113 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f401cc630cc0349b05e42ad04f05cffdcd157a3bea09429537977246d2f24655`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1768176000'
# Wed, 28 Jan 2026 18:01:53 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 28 Jan 2026 18:01:53 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 28 Jan 2026 18:01:53 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Jan 2026 18:01:53 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Wed, 28 Jan 2026 18:01:53 GMT
WORKDIR /tmp
# Wed, 28 Jan 2026 18:02:09 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 28 Jan 2026 18:02:09 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 28 Jan 2026 18:02:09 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:1029f5ddc0d24726f1cefbb8def7a88f8ec819a1fdc4c05ce523011b4b73c72d`  
		Last Modified: Tue, 13 Jan 2026 00:41:14 GMT  
		Size: 48.4 MB (48366072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77f656ffd9a81119be3b2c887541c6aab59080f38a2ceefa21844d92597a1fd0`  
		Last Modified: Wed, 28 Jan 2026 18:02:29 GMT  
		Size: 53.8 MB (53815008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ff23eee8e25c35355b7367992f025c32e0be5d5766ee2c98ec0d7c33b61e0a0`  
		Last Modified: Wed, 28 Jan 2026 18:02:30 GMT  
		Size: 81.1 MB (81138391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a31beec40e390d3f9e4638b0c63031b4bacc455da664882ce99ecd03d72e198a`  
		Last Modified: Wed, 28 Jan 2026 18:02:26 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:44c54cfaf4627df23a8db1b90f610a92c4f8425e11b595f4538f783b3406805b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7517916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b5951738479cf80319efd61d06c9e768120ff2206871fcc81ee621ecfc980ac`

```dockerfile
```

-	Layers:
	-	`sha256:fb24680e803dbccb53f827fce96f504fa238b151f49afb0a6ef724f7b8cd33bd`  
		Last Modified: Wed, 28 Jan 2026 18:02:27 GMT  
		Size: 7.5 MB (7503606 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:930889318a63b213368dfcd81d0e32470144a94e2dbfc639a31346848e764124`  
		Last Modified: Wed, 28 Jan 2026 18:02:26 GMT  
		Size: 14.3 KB (14310 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-bookworm` - linux; ppc64le

```console
$ docker pull clojure@sha256:02dc6f7eb84a76bd7771cc512285d8664614410b04baa2063175c747b6f18621
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.5 MB (191490753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29544c7169c4c7cbee830baa852ae5498db641aa7bb140bb0c9cf472c0959748`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1768176000'
# Wed, 28 Jan 2026 18:00:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 28 Jan 2026 18:00:33 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 28 Jan 2026 18:00:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Jan 2026 18:00:33 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Wed, 28 Jan 2026 18:00:33 GMT
WORKDIR /tmp
# Wed, 28 Jan 2026 18:01:19 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 28 Jan 2026 18:01:20 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 28 Jan 2026 18:01:20 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:7fcf9f2b462d6af06c3ad2420b999e6b092984c4723ebac480c428a5d837d3b7`  
		Last Modified: Tue, 13 Jan 2026 00:40:14 GMT  
		Size: 52.3 MB (52327376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b99bb83329a0c5fc6acd22d5872bbf056865238fc896237be5785fd14f1bcf9d`  
		Last Modified: Wed, 28 Jan 2026 18:02:08 GMT  
		Size: 52.2 MB (52175138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d112b5d2c3e3696ea1cb216c3fc6dd138abe09849fc424fe7f8e72cd1e82b518`  
		Last Modified: Wed, 28 Jan 2026 18:02:08 GMT  
		Size: 87.0 MB (86987596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7964e0031882735fca1d411effebd5ffc926d7b417c818f8c7bd85dc9a0c8dac`  
		Last Modified: Wed, 28 Jan 2026 18:02:05 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:1694b7eaead272c90c68f3aeba606752c44c7426340ac6fdae3147abaa1e7050
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7517196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d69f8901a5ea347acc6222217ee89f1439f7dff326c1835cd18a5f6e3d3eb49`

```dockerfile
```

-	Layers:
	-	`sha256:3c47527c5899c7dafad73012560b2c700af3ac6e59c573ba9c677bfbf13311fb`  
		Last Modified: Wed, 28 Jan 2026 18:02:05 GMT  
		Size: 7.5 MB (7502954 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d090986c9af6b40791c1694177cf2e73d26e7f2f4522f1433a76603031e9d898`  
		Last Modified: Wed, 28 Jan 2026 18:02:04 GMT  
		Size: 14.2 KB (14242 bytes)  
		MIME: application/vnd.in-toto+json
