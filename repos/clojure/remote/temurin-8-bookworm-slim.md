## `clojure:temurin-8-bookworm-slim`

```console
$ docker pull clojure@sha256:b48b8ec1367f157df572e24d585584ecdcb51eb5cab23c1768a373ea7ac19990
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-8-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:1d4a9fdc76e02044597467d3359eea73b09887568b46d8cd604cba534c325579
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **202.2 MB (202243526 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0db8e362d35dc93c674cfe56e786306039600615a6eb69416ac6cab74b511a4c`
-	Default Command: `["clj"]`

```dockerfile
# Thu, 03 Oct 2024 17:49:34 GMT
ADD file:90b9dd8f12120e8b2cd3ece45fcbe8af67e40565e2032a40f64bd921c43e2ce7 in / 
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["bash"]
# Thu, 03 Oct 2024 17:49:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 03 Oct 2024 17:49:34 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Oct 2024 17:49:34 GMT
ENV CLOJURE_VERSION=1.12.0.1479
# Thu, 03 Oct 2024 17:49:34 GMT
WORKDIR /tmp
# Thu, 03 Oct 2024 17:49:34 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "94f29b9b66183bd58307c46fb561fd9e9148666bac13a4518a9931b6f989d830 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:a480a496ba95a197d587aa1d9e0f545ca7dbd40495a4715342228db62b67c4ba`  
		Last Modified: Thu, 17 Oct 2024 00:23:58 GMT  
		Size: 29.1 MB (29126289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0d292b1dffafd23095a248aa6736e3551fb520b1ede0c74b31afd625338dd99`  
		Last Modified: Thu, 24 Oct 2024 01:59:07 GMT  
		Size: 103.6 MB (103633964 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f79939ae42f357f78f52fb0c9344c318c6d960c99d5220513a8f8f92ab211818`  
		Last Modified: Thu, 24 Oct 2024 01:59:07 GMT  
		Size: 69.5 MB (69482627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f45493f3849eef134651a62120c6fcae40dacd15df1b7e94a0185e57bf53322c`  
		Last Modified: Thu, 24 Oct 2024 01:59:06 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:e76a0c3b27c6f4f47297055907c9a7093c3fe541f69a7a8599be0278c8b725ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5056862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:771551db664ef2ffacc837e8039fab9f10654a42fc36f6d5096a338272d3bb53`

```dockerfile
```

-	Layers:
	-	`sha256:be3a3532dd0ca96d4a86e30e08f0bb054fe91de3956fc1323b93b6a74c9810d0`  
		Last Modified: Thu, 24 Oct 2024 01:59:06 GMT  
		Size: 5.0 MB (5042762 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4994aaf6bdaee06f90f9921ca69956eaef8ccf771118782c101ef860f616ee68`  
		Last Modified: Thu, 24 Oct 2024 01:59:06 GMT  
		Size: 14.1 KB (14100 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:7e1b53f7ebd1ba4ee567361b256fbf90293fc9775b4783fa2d062b8b5f5292b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **201.3 MB (201250038 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a45a2ba09b447a4a28964360c0fc4b3c9cb4b40a4a62778c3c7c44fc7527fa5a`
-	Default Command: `["clj"]`

```dockerfile
# Thu, 03 Oct 2024 17:49:34 GMT
ADD file:702193928cded0bcec5edbf4a5660961e7caef8c9d9cafea3337b7f6720c4464 in / 
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["bash"]
# Thu, 03 Oct 2024 17:49:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 03 Oct 2024 17:49:34 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Oct 2024 17:49:34 GMT
ENV CLOJURE_VERSION=1.12.0.1479
# Thu, 03 Oct 2024 17:49:34 GMT
WORKDIR /tmp
# Thu, 03 Oct 2024 17:49:34 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "94f29b9b66183bd58307c46fb561fd9e9148666bac13a4518a9931b6f989d830 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:83d624c4be2db5b81ae220b6b10cbc9a559d5800fd32556f4020727098f71ed0`  
		Last Modified: Thu, 17 Oct 2024 01:14:39 GMT  
		Size: 29.2 MB (29156341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2aa401c93c47e90bf34a831f8ca7797d9e56e8ef8fbe8eff2482c076a1fb2d97`  
		Last Modified: Thu, 24 Oct 2024 08:52:33 GMT  
		Size: 102.7 MB (102747729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ad6590b03fdc729a5b06919c4f6ab6152bfec02c4023994555677123de51043`  
		Last Modified: Thu, 24 Oct 2024 08:58:42 GMT  
		Size: 69.3 MB (69345323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a7760046391ad4246805cd1c2a4452cc93813fd156a17d270851a54d2d3ed5b`  
		Last Modified: Thu, 24 Oct 2024 08:58:40 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:3f9df6acc0378e9dc0dfe545902c3aacefef1209f0336e7d17fa65c86de4ad66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5063468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:354d64d1f848925e7f7cd403c189036494f2e7fe44615431dcb34f5b6589e206`

```dockerfile
```

-	Layers:
	-	`sha256:b0351716bff807daa147c1ddd1e15410fb51ec5d0959a7933989c99032123340`  
		Last Modified: Thu, 24 Oct 2024 08:58:40 GMT  
		Size: 5.0 MB (5049227 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:77cb9260372b26d9a61e94baa9c4b4cc45957df22de71e483c653f44197193f0`  
		Last Modified: Thu, 24 Oct 2024 08:58:40 GMT  
		Size: 14.2 KB (14241 bytes)  
		MIME: application/vnd.in-toto+json
