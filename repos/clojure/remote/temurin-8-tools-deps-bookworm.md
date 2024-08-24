## `clojure:temurin-8-tools-deps-bookworm`

```console
$ docker pull clojure@sha256:8583e9e145a314659c58e750282f36ae2e0c8ba19d3bedae0aa1d6d86a2c05a3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:1bacb1500b53375539d3b53ac58cb8d3b44d09711e9b2a5af9dd856782ec319f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.6 MB (233620128 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c65429e7c23146186b0d630d47fb6f2f54cbb922596a820a3c8113347af20215`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 07 Aug 2024 18:04:12 GMT
ADD file:0d5bdf84bbcdfa95d42190537e3cad2c0a5876f9127fae6a1d1c485d3539c77d in / 
# Wed, 07 Aug 2024 18:04:12 GMT
CMD ["bash"]
# Wed, 07 Aug 2024 18:04:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 07 Aug 2024 18:04:12 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 07 Aug 2024 18:04:12 GMT
ENV CLOJURE_VERSION=1.11.4.1474
# Wed, 07 Aug 2024 18:04:12 GMT
WORKDIR /tmp
# Wed, 07 Aug 2024 18:04:12 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "b23a784c048e4a5b1fc4bcddaea07abcf476621a97d98bbf4f4726c3375d6e98 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:903681d87777d28dc56866a07a2774c3fd5bf65fd734b24c9d0ecd9a13c9f636`  
		Last Modified: Tue, 13 Aug 2024 00:23:26 GMT  
		Size: 49.6 MB (49554080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0363768455b327256b65e9a3e1595be5f2d3d3b7701184d8de667c1ff8e1da60`  
		Last Modified: Fri, 23 Aug 2024 20:02:12 GMT  
		Size: 103.6 MB (103611892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d7aa81fbff0e8bac3ab80a5627cde7fcbeb8b9458da10b04fb1c87c56b8eeec`  
		Last Modified: Fri, 23 Aug 2024 20:02:12 GMT  
		Size: 80.5 MB (80453509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:928a67ce8b8e8be594f154c5a2f41345dd6a016b576afba7b1d4081c8fed52cc`  
		Last Modified: Fri, 23 Aug 2024 20:02:09 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:7d911e6104e3e4b553f080c7957d0b7db50ffc87fb2f385ece0e387fbd8ca161
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7039429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8f3a39f9eb4ec4a0d674cfc7e2b4532235026270432cb60c28eb6141070fdd7`

```dockerfile
```

-	Layers:
	-	`sha256:f9f5aa3f6625af420a557738f93ac89f2797e27b8726f92974902cc9d042617a`  
		Last Modified: Fri, 23 Aug 2024 20:02:10 GMT  
		Size: 7.0 MB (7025577 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:320daf1e3d5b099129e7dafc9c111f5986e13b80d88ea078ba8a356be8714a00`  
		Last Modified: Fri, 23 Aug 2024 20:02:09 GMT  
		Size: 13.9 KB (13852 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:6e8d69dae76343f33da7b072e4a033c756f4b407c4168cd44617c808833456a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.5 MB (232516912 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:056906c0df352d6963f6aa3bd4f3383fcd25efe0309f9ccc248203a73834b9f1`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 07 Aug 2024 18:04:12 GMT
ADD file:e81dd8b32e45ea6e761021a3e01b6efd339dd9248a2036dc4b51a2c1de560b4c in / 
# Wed, 07 Aug 2024 18:04:12 GMT
CMD ["bash"]
# Wed, 07 Aug 2024 18:04:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 07 Aug 2024 18:04:12 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 07 Aug 2024 18:04:12 GMT
ENV CLOJURE_VERSION=1.11.4.1474
# Wed, 07 Aug 2024 18:04:12 GMT
WORKDIR /tmp
# Wed, 07 Aug 2024 18:04:12 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "b23a784c048e4a5b1fc4bcddaea07abcf476621a97d98bbf4f4726c3375d6e98 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:7b24851aa36de07cd94173b8e2052846573dacc3b241620d713254e647352394`  
		Last Modified: Tue, 13 Aug 2024 00:42:24 GMT  
		Size: 49.6 MB (49588592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df82fcaf825bfd95bf3f6a60bf33b338e56c6f56d64178e49f0cba774c6851aa`  
		Last Modified: Sat, 17 Aug 2024 05:50:41 GMT  
		Size: 102.7 MB (102729249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f746f1a501618a4a44c5b26b39e9abbdba8041db75216d0611702cacac1e7608`  
		Last Modified: Sat, 17 Aug 2024 05:56:15 GMT  
		Size: 80.2 MB (80198427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22810dc900a5792ba8b6288c5805112f448f03e6edf91c827e68f28b0430292b`  
		Last Modified: Sat, 17 Aug 2024 05:56:13 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:1c9775c2401681b28c72bd3f3ccbf25df7bc11952deaebf0e40dd22f7fd5be52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7046350 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06d32b38cf1d6086503ea32d34872ec7292142c10aed83fe3a4832f01877dbe0`

```dockerfile
```

-	Layers:
	-	`sha256:30558b1e44a64d5a4ea68e90396e92f488ed3acbc4f46e0ad8b7606c69cbc042`  
		Last Modified: Fri, 23 Aug 2024 20:46:55 GMT  
		Size: 7.0 MB (7031964 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:62ff756d2945c891c2e320b622c8637c7e80b0842accf9effe2abffc587d0a58`  
		Last Modified: Fri, 23 Aug 2024 20:46:55 GMT  
		Size: 14.4 KB (14386 bytes)  
		MIME: application/vnd.in-toto+json
