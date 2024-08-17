## `clojure:temurin-8-tools-deps-bookworm`

```console
$ docker pull clojure@sha256:56871c9f390fdd7313f0b41fb7f37d571a256e73d2935780d1cc05bf88d10c15
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:16f2bb9baebc3aa1e1020440c3db8b3e289fb7f9f5097520fcb9bb361b9e8d31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.6 MB (233620627 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73c08cd7ebcce8021eaf4f7dee22fd78cf85bc49d391182a2e07be488f5ad863`
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
	-	`sha256:2f988fcae5f7c2e5cd901cdd3f9f6818542a92e517485bbbb08de84d6a17a570`  
		Last Modified: Sat, 17 Aug 2024 01:59:27 GMT  
		Size: 103.6 MB (103611892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3ee99793f3ad664ac032a480f8c5096ad3dbfefb2d7dbc92d12162a12552d0d`  
		Last Modified: Sat, 17 Aug 2024 01:59:26 GMT  
		Size: 80.5 MB (80454010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99c6f1a6e98ba1c206fd49a3c88c620a2ffd6f8f399612e49666bc873e5c1d7c`  
		Last Modified: Sat, 17 Aug 2024 01:59:25 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:2a6fe04c5c2b207c94b9af83df38d78fc65cd08b16db8cc65e902011a9a73481
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7039429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a14a532a8a8ddbf7de4c0b5654048b4b91fb307f324a8b94d842a666574ab975`

```dockerfile
```

-	Layers:
	-	`sha256:474156e3799053d6319420e9e991caef2bb91cd2ce3a6e4e451ed9dd02e82707`  
		Last Modified: Sat, 17 Aug 2024 01:59:25 GMT  
		Size: 7.0 MB (7025577 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5acad79f815ea518902ff35e0ef95f6e46fc7ef50114db8ccc20bbb7599c19e1`  
		Last Modified: Sat, 17 Aug 2024 01:59:25 GMT  
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
$ docker pull clojure@sha256:6e9c28b0b86b31c4ef3a2ee24853deaaf0e6f69f7d918f59aaac24604462b0d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7046351 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:506517cc28d02d213b667d79ef07cfbab73fd98c373fc07263ef016d2a9f40cd`

```dockerfile
```

-	Layers:
	-	`sha256:59664fb301ffeb13db68992907eb93f396b0e1f7987a446c75c28cd24e1ba09a`  
		Last Modified: Sat, 17 Aug 2024 05:56:13 GMT  
		Size: 7.0 MB (7031964 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:965d679a1e7b4305705b83a5499f79ac7250c2ade0e7bb74982fe690988a8ba9`  
		Last Modified: Sat, 17 Aug 2024 05:56:13 GMT  
		Size: 14.4 KB (14387 bytes)  
		MIME: application/vnd.in-toto+json
