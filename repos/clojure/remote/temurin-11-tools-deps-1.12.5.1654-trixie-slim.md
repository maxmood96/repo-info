## `clojure:temurin-11-tools-deps-1.12.5.1654-trixie-slim`

```console
$ docker pull clojure@sha256:b66e36a6897f01e450979dc85a5ead592653dba6aed7d97de1fa79174a78e2d8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `clojure:temurin-11-tools-deps-1.12.5.1654-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:39737d6675a0983dfce2d4f62d59969ba25f0b7106e3eb9fd6c89e88e89ae089
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.6 MB (244618847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94bc9e39435b7bc7b37745eed49f09fa8b45b2875f66b734e0d36344e4115922`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1779062400'
# Thu, 04 Jun 2026 17:45:39 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 Jun 2026 17:45:39 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 04 Jun 2026 17:45:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Jun 2026 17:45:39 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Thu, 04 Jun 2026 17:45:40 GMT
WORKDIR /tmp
# Thu, 04 Jun 2026 17:45:55 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 04 Jun 2026 17:45:55 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 04 Jun 2026 17:45:55 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:5b4d6ff92fc4e14e911b7753c954fac965d48c40fe1075758d284148ccace970`  
		Last Modified: Tue, 19 May 2026 22:37:05 GMT  
		Size: 29.8 MB (29779926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9af83e5e1075a50c32bfe63a9a5ff4df3efc4db505663c9b870aea9c59fc5bc`  
		Last Modified: Thu, 04 Jun 2026 17:46:18 GMT  
		Size: 145.9 MB (145886219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2261e543bd15c256e491eecd0ee08a5ed9819fa229ac799e0de68f64362de47`  
		Last Modified: Thu, 04 Jun 2026 17:46:16 GMT  
		Size: 69.0 MB (68952055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d88ee0150df282bd24d3ce8e6f832ae8bb0f092422ffde2d2d29de12ccf9e58`  
		Last Modified: Thu, 04 Jun 2026 17:46:13 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.5.1654-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:980208f2f1014bf16695b4e6c719cc32bbf91eee91a15e90aa32db2318259179
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5291153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bad92bb77d1e4126cf647e0103b94765172b2d0cd606f51a783639adc328b46`

```dockerfile
```

-	Layers:
	-	`sha256:f21f1871e53e4b7cce8074490b61fb3ccc04612da7bd0bd29577f8bb4685babd`  
		Last Modified: Thu, 04 Jun 2026 17:46:13 GMT  
		Size: 5.3 MB (5276758 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:749c86f7b4be14e0b703d697b545a831fe9d72316a57b1eeeb6680249f2058af`  
		Last Modified: Thu, 04 Jun 2026 17:46:13 GMT  
		Size: 14.4 KB (14395 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-1.12.5.1654-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:53da99569a272808695f21c9b32c5ed55f41e327ef406a4e4503dfbc46a4620c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.5 MB (241502103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f29d53ac9e6e252ca6155ff3b8fe5972176769d3910e75e5fb74bd13876baa4`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1779062400'
# Thu, 04 Jun 2026 17:45:35 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 Jun 2026 17:45:35 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 04 Jun 2026 17:45:35 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Jun 2026 17:45:35 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Thu, 04 Jun 2026 17:45:35 GMT
WORKDIR /tmp
# Thu, 04 Jun 2026 17:45:52 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 04 Jun 2026 17:45:52 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 04 Jun 2026 17:45:52 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:cda3d70ae7d7c3d0b3b57a99a2085f9d93e919a846913dc6517a420b348c123d`  
		Last Modified: Tue, 19 May 2026 22:36:58 GMT  
		Size: 30.1 MB (30141919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3334c3e2ac809452f5fad19898f0399fd679673a3fa769269cb209632e1dca6d`  
		Last Modified: Thu, 04 Jun 2026 17:46:16 GMT  
		Size: 142.6 MB (142582230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:694699710e3a26e0f2c33759fddcbe2fe5b08ff6e3ee8370274afcf91b15ea86`  
		Last Modified: Thu, 04 Jun 2026 17:46:14 GMT  
		Size: 68.8 MB (68777309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc1bf2dcf3b57e6f87dde2da81cc2827927da2555ecdd32d04017f6c487227b6`  
		Last Modified: Thu, 04 Jun 2026 17:46:11 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.5.1654-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:d8327d254ab4c787a3d554fa7ba4e321fc96b31bd00d29fc5bb00d42ed123a9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5297652 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8662bd3ccf97921a429881442d46edf6443923ccaef9a582cd3b3eae2fe60abd`

```dockerfile
```

-	Layers:
	-	`sha256:b6463fc4a48355b9b732edb8fd20b80bbc62e7dff1566907f5096a8729c298d5`  
		Last Modified: Thu, 04 Jun 2026 17:46:11 GMT  
		Size: 5.3 MB (5283137 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:83da7c785ad3a8e525534c6a1fc0f579895c814e5ce18799175a7e128df0e8d2`  
		Last Modified: Thu, 04 Jun 2026 17:46:11 GMT  
		Size: 14.5 KB (14515 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-1.12.5.1654-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:e6de9f17ef6b80531828de95dd455b3fc8359d8e2017a9e15d301e9aadd515c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.1 MB (241080216 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f83617be5e4aeb106b1373c257951c6e78968687dcf58b66218843f76b00ca2`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1779062400'
# Thu, 04 Jun 2026 17:50:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 Jun 2026 17:50:49 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 04 Jun 2026 17:50:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Jun 2026 17:50:49 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Thu, 04 Jun 2026 17:50:49 GMT
WORKDIR /tmp
# Thu, 04 Jun 2026 17:51:38 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 04 Jun 2026 17:51:38 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 04 Jun 2026 17:51:38 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:4dea3595b4b879a8f487420dc7e601b4fe79f2769fed7f891c99b52fea019c27`  
		Last Modified: Tue, 19 May 2026 22:37:58 GMT  
		Size: 33.6 MB (33600453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:814209118c1f9988310c804cfede565b6de88c2bb18bc3b89f0db3f5461a6e45`  
		Last Modified: Thu, 04 Jun 2026 17:52:18 GMT  
		Size: 133.1 MB (133110168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6fe03e819f7cb6cd541206c85a83f563b1a8ddad2ba6e83f8fa1c59d29899df`  
		Last Modified: Thu, 04 Jun 2026 17:52:17 GMT  
		Size: 74.4 MB (74368948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae83a516b4676f3a601a793ef918c4c55bb1bd3ac2aa9efe9bef897f50d2745c`  
		Last Modified: Thu, 04 Jun 2026 17:52:13 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.5.1654-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:fbcb635204239d89338fb2f30c60cd817326eacb705dc93e703400f088eebfff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5294959 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e26f7de14fb14f0238fe1ccc43306771e0a00f9e39eb73b4c67228494c8795ce`

```dockerfile
```

-	Layers:
	-	`sha256:817c3ea6e920e3ec6de18d4353a31f08071a889c4b94ceb71e8227cd12ecbd3c`  
		Last Modified: Thu, 04 Jun 2026 17:52:14 GMT  
		Size: 5.3 MB (5280514 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e60c1bea9cdd6ac3efefb2aea35f0d02c17c03544685e3b63569caac8547794e`  
		Last Modified: Thu, 04 Jun 2026 17:52:13 GMT  
		Size: 14.4 KB (14445 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-1.12.5.1654-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:08bbee5cfa6faa28d4f8b0b37c7eb359e6766fcf9cd9cf77c7628335c818ba8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.4 MB (226430899 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bbd8b0400f60fa8e9558e7afb89e7bf0d42aba6dbd1ba6b6a4f9e7d28cb6312`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1779062400'
# Thu, 04 Jun 2026 17:41:28 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 Jun 2026 17:41:28 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 04 Jun 2026 17:41:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Jun 2026 17:41:28 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Thu, 04 Jun 2026 17:41:28 GMT
WORKDIR /tmp
# Thu, 04 Jun 2026 17:41:50 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 04 Jun 2026 17:41:50 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 04 Jun 2026 17:41:50 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:3a7bf300ab749fc8aaa5ec872160f889b9f1fd11db31bb5e8fe4d9ec131347b0`  
		Last Modified: Tue, 19 May 2026 22:36:59 GMT  
		Size: 29.8 MB (29845924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74f38a9a10021642d38304ca2f4835906120ee9f5d7b6ae1fcbc21934d29f896`  
		Last Modified: Thu, 04 Jun 2026 17:42:21 GMT  
		Size: 126.7 MB (126651735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46e1eb530b3b2a18a8c6f764d2704c9f663551adf3d04e211ff75132e9962088`  
		Last Modified: Thu, 04 Jun 2026 17:42:19 GMT  
		Size: 69.9 MB (69932595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97902c5b6619e71b6ba5e9b84c9cce519051feecf1fc9f20cb0fe14596d577df`  
		Last Modified: Thu, 04 Jun 2026 17:42:17 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.5.1654-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:f5446d305c4874a11143dc3e69e0f7ac1e2ba130d572c443c750be649b89ee77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5287082 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30798054051d482025c77d1b2479557bee1fcc44cf7db508a1fb52d6263b33b6`

```dockerfile
```

-	Layers:
	-	`sha256:47186d4da014363270964810b162dee3a1497fc38e08bff8a7f703379d5f3eb9`  
		Last Modified: Thu, 04 Jun 2026 17:42:17 GMT  
		Size: 5.3 MB (5272686 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3a56745ee80d61597c44825d6bb005d768393ff87b3ae45c1b7814368a7cdbd0`  
		Last Modified: Thu, 04 Jun 2026 17:42:17 GMT  
		Size: 14.4 KB (14396 bytes)  
		MIME: application/vnd.in-toto+json
