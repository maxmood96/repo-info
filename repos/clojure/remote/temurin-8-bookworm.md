## `clojure:temurin-8-bookworm`

```console
$ docker pull clojure@sha256:4ddbbf4459c4f197aa2bff17a9566be883e21808ace7d08f33a99a674a82452b
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
$ docker pull clojure@sha256:8c78f1d33dc2cb7c7e8d002ee495e2970162a00f3aca3d7eaaf327f1051a727f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.4 MB (184361453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72dfced8f3c3ed51e91d325abd6825a19174f48a8037af74b37e8cdd5313ca18`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 03:20:54 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 Jan 2026 03:20:54 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 Jan 2026 03:20:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 03:20:54 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Tue, 13 Jan 2026 03:20:54 GMT
WORKDIR /tmp
# Tue, 13 Jan 2026 03:21:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 13 Jan 2026 03:21:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 13 Jan 2026 03:21:11 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:c1be109a62df95316ceac87ea501079f32e17f36b636865a860841b7db06100c`  
		Last Modified: Tue, 13 Jan 2026 00:41:40 GMT  
		Size: 48.5 MB (48481622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f3646e204f2800699242acbd30747c62a455ded849d5efbb22ef3d0f2949824`  
		Last Modified: Tue, 13 Jan 2026 03:21:54 GMT  
		Size: 54.7 MB (54733365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2662e83ad75173a698ae9a56b401a7ba19bb429910c4969bc2864e44bbc0cbfe`  
		Last Modified: Tue, 13 Jan 2026 03:21:43 GMT  
		Size: 81.1 MB (81145822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf1206e30e7fa4f655a3c35d83ceb75104705cffc551595472f7f5d749446911`  
		Last Modified: Tue, 13 Jan 2026 03:21:36 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:7c5829155879e9bdaee13bb9c54e0216b12e1fd6883f3672d955fbb1e74459c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7511337 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73f7ca135e529ee6467c36cd1e04ef33f7ced20d865b60761ddfd9f09e9b754e`

```dockerfile
```

-	Layers:
	-	`sha256:4f8e0c58e5d6f2df05ed1dd5842c0b5090f0f890ffc060c3e0b318a4e0c5482c`  
		Last Modified: Tue, 13 Jan 2026 07:47:34 GMT  
		Size: 7.5 MB (7497143 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:974d9f64b72ec232c93d2208e00af6915b71012cfe80bae803bd4765668cd10e`  
		Last Modified: Tue, 13 Jan 2026 07:47:35 GMT  
		Size: 14.2 KB (14194 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:488c47760023830625ddfaf7642aa9e0c79a02289d64c5fc0377e937b622c66d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.3 MB (183320857 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6506c522b76cc2278e5598b9d8054d72864a8e9773ea98c32acef2c21e3d15af`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 03:26:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 Jan 2026 03:26:52 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 Jan 2026 03:26:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 03:26:52 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Tue, 13 Jan 2026 03:26:52 GMT
WORKDIR /tmp
# Tue, 13 Jan 2026 03:28:30 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 13 Jan 2026 03:28:30 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 13 Jan 2026 03:28:30 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:1029f5ddc0d24726f1cefbb8def7a88f8ec819a1fdc4c05ce523011b4b73c72d`  
		Last Modified: Tue, 13 Jan 2026 00:41:34 GMT  
		Size: 48.4 MB (48366072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a2f99609557d992fd2475784f3548dc4b1c57cd7b761c5b66cb56d67e374ad4`  
		Last Modified: Tue, 13 Jan 2026 03:27:34 GMT  
		Size: 53.8 MB (53814993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca3317ea7b60e4c13c5c803a133b9f53eeae417a902535afb661dc24476b33cd`  
		Last Modified: Tue, 13 Jan 2026 03:29:01 GMT  
		Size: 81.1 MB (81139148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ea4d72a17642b4e99ef8610ef657e1a14d7bd8df4c044664df501f72475e153`  
		Last Modified: Tue, 13 Jan 2026 03:28:52 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:061d445ab5acc441c0a7ad81fab58a0a8adc291273b207f5de0dd2e7b4ea3954
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7517916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4771f8ed2fa9fc98dc86431ec527779ae678e265b295b3600abab0df95ccafbf`

```dockerfile
```

-	Layers:
	-	`sha256:da24c7ca3f2e4b04662c6044aa3d6a25eaca49074314a00d161cc4b298465136`  
		Last Modified: Tue, 13 Jan 2026 07:47:42 GMT  
		Size: 7.5 MB (7503604 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1126ae9c21a035bfab27e2ea99bc0dbcbe8fe4d83ce6052e2aeba5ba1b6cd37f`  
		Last Modified: Tue, 13 Jan 2026 07:47:43 GMT  
		Size: 14.3 KB (14312 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-bookworm` - linux; ppc64le

```console
$ docker pull clojure@sha256:3ff51a47981cb19c054901db7e27e49ca75dd3618bbd0f84cc541c31e32212b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.5 MB (191489870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c7ca8946b02b67365e72885542c23d9b0d1e3f7fda36f6986d3a9b79c07d2b2`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 05:31:07 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 Jan 2026 05:31:07 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 Jan 2026 05:31:07 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 05:31:07 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Tue, 13 Jan 2026 05:31:07 GMT
WORKDIR /tmp
# Tue, 13 Jan 2026 05:34:14 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 13 Jan 2026 05:34:15 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 13 Jan 2026 05:34:15 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:7fcf9f2b462d6af06c3ad2420b999e6b092984c4723ebac480c428a5d837d3b7`  
		Last Modified: Tue, 13 Jan 2026 00:40:39 GMT  
		Size: 52.3 MB (52327376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d020e47d05d77ed95970b2139c4917941d14aed26d8a5bc05d664cbb0b68c5d`  
		Last Modified: Tue, 13 Jan 2026 05:32:38 GMT  
		Size: 52.2 MB (52175143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b00f881cfdc6b3e93f03633e1956f51075a23e55af75870d6af30539cdf077d`  
		Last Modified: Tue, 13 Jan 2026 05:35:20 GMT  
		Size: 87.0 MB (86986706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb6ed7e353c5c55868b5f3ab4c5d68e67f2f8daf739cf3bd8d22968865bfcc7a`  
		Last Modified: Tue, 13 Jan 2026 05:35:07 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:e2335faa7893c24d1cadab456d385b53a0a42108b0985a98a43450ea59d3c932
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7516394 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec2d3846623be6d9eb5a74a5852a2f7d67b79ceb34d08138ae47a43ebf6b3d6d`

```dockerfile
```

-	Layers:
	-	`sha256:88d21c46844be4e4fa5a0cc6e134df2a92b4ed0c31b2efb269361f54eb615d44`  
		Last Modified: Tue, 13 Jan 2026 07:47:49 GMT  
		Size: 7.5 MB (7502952 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5c040e0b1e2f1a3c06e02171ed6c82057fae93b24e6cb20ca6cdef84e9197b2f`  
		Last Modified: Tue, 13 Jan 2026 07:47:50 GMT  
		Size: 13.4 KB (13442 bytes)  
		MIME: application/vnd.in-toto+json
