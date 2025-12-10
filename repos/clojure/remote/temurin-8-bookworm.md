## `clojure:temurin-8-bookworm`

```console
$ docker pull clojure@sha256:9b79614d4c6a5bf530ebf6877bb02e6ca4e572879ef8687ccac9d537fb626c1f
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
$ docker pull clojure@sha256:177219b585146452067fe6c058c88d375bb5371e651653575eec03bb07c25700
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.4 MB (184360767 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f46a80fe1a233698a8c0d49bd0f75e19f8f341165b3c37e3556c408251dd776f`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1765152000'
# Mon, 08 Dec 2025 23:50:02 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 08 Dec 2025 23:50:02 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 08 Dec 2025 23:50:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Dec 2025 23:50:02 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Mon, 08 Dec 2025 23:50:02 GMT
WORKDIR /tmp
# Mon, 08 Dec 2025 23:50:18 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 08 Dec 2025 23:50:18 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 08 Dec 2025 23:50:18 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:c8443a297fa42e27cb10653777dd5a53f82a65fbc8b2d33f82b8722199f941d3`  
		Last Modified: Mon, 08 Dec 2025 22:16:25 GMT  
		Size: 48.5 MB (48480736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbc64fb9e4c8904524c0e6a81dfdfc06c1bb180140216432296eea166c5df800`  
		Last Modified: Mon, 08 Dec 2025 23:50:42 GMT  
		Size: 54.7 MB (54733371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0d002bc1c38faadb0c74463dadf83cf9bf5b30ca869c401431b904095828637`  
		Last Modified: Mon, 08 Dec 2025 23:50:50 GMT  
		Size: 81.1 MB (81146017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a01fdfb4c5b0bbb5250e02d620cab143bebf3ff8b0447ace16d1168fc6592b6`  
		Last Modified: Mon, 08 Dec 2025 23:50:44 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:45bc4a120c198deed3f965e51f05a45931594a36d19ae7bf0280abbcbc2ce400
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7510694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0cdff05053447f270a9c5c2f96d08ffe7f8356f200bc5395678e7b6dbea17ba4`

```dockerfile
```

-	Layers:
	-	`sha256:7bfb3f72f795e2e1fb55e4b8c0186610ceec1a65fcced49bcc21d01cdb441c7b`  
		Last Modified: Tue, 09 Dec 2025 04:47:46 GMT  
		Size: 7.5 MB (7496500 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5438ad5c39f3ef897f3ad91d6a39ffac10e8aaacae954250422224bb442c4262`  
		Last Modified: Tue, 09 Dec 2025 04:47:47 GMT  
		Size: 14.2 KB (14194 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:368a46590c129cea5b30e23d60c4a58d5089bd44f74ed35ff2a9c412d9875be1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.2 MB (183205690 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03d508b23dfc56a38e507c22fc2ddd99b080390f9375682a92e1875c93d08bb3`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1765152000'
# Mon, 08 Dec 2025 23:57:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 08 Dec 2025 23:57:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 08 Dec 2025 23:57:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Dec 2025 23:57:36 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Mon, 08 Dec 2025 23:57:36 GMT
WORKDIR /tmp
# Mon, 08 Dec 2025 23:57:52 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 08 Dec 2025 23:57:52 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 08 Dec 2025 23:57:52 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:7f2b9668af76f73927725e2d1fb5d7224604d8c4c42cb8cdecb502257d9101c4`  
		Last Modified: Mon, 08 Dec 2025 22:16:59 GMT  
		Size: 48.4 MB (48359071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7f83373550d3213d2659b330594d1075f74611c56852535bb168e40cd21ccb8`  
		Last Modified: Mon, 08 Dec 2025 23:58:22 GMT  
		Size: 53.8 MB (53815011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46d8ee0e8707728be84456a0312872acb938d653792ce530a02b3109c37d7e24`  
		Last Modified: Mon, 08 Dec 2025 23:58:25 GMT  
		Size: 81.0 MB (81030965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58cb96d172702dcf5da404935ee3e7bce7c760ee22b5ea6bf4631c77187fd0ed`  
		Last Modified: Mon, 08 Dec 2025 23:58:20 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:5215a16ff3757e31163f179a7d3345578d2d1851565d947581de286b154dc6e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7517273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:299cada5081fb4572bacd6d1bf21dd355bbcd83fbe86ac188fb8c25429f1bdf7`

```dockerfile
```

-	Layers:
	-	`sha256:4b9a997f78d9ed42d9f530a319840b43b660739cfc505d347e01f2c726dbd9e1`  
		Last Modified: Tue, 09 Dec 2025 04:47:53 GMT  
		Size: 7.5 MB (7502961 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c238c8081eb10c3efbfc18cad4664ebd53f3c83471c80a6664d5c6a5001078d9`  
		Last Modified: Tue, 09 Dec 2025 04:47:53 GMT  
		Size: 14.3 KB (14312 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-bookworm` - linux; ppc64le

```console
$ docker pull clojure@sha256:e760d17996ab222aa5e10713913b86801e91229511fd00c12f65ad94dab5f769
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.5 MB (191488788 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c10608c0f6d501b10e5ae2a7f36d6dd344db454e063aea6b833de201a2aaef6`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1765152000'
# Mon, 08 Dec 2025 22:37:07 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 08 Dec 2025 22:37:07 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 08 Dec 2025 22:37:07 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Dec 2025 22:37:07 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Mon, 08 Dec 2025 22:37:08 GMT
WORKDIR /tmp
# Mon, 08 Dec 2025 22:39:02 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 08 Dec 2025 22:39:02 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 08 Dec 2025 22:39:02 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:c088128ea77bb5c706bb00930020ea2fba147060275f49c5a7be6b54af5ca7c8`  
		Last Modified: Mon, 08 Dec 2025 22:17:06 GMT  
		Size: 52.3 MB (52326977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6a51c77f8794a7a48d981ba475763915c444e47af96f90a51cb42c060ef190d`  
		Last Modified: Mon, 08 Dec 2025 22:38:19 GMT  
		Size: 52.2 MB (52175143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a83649973de83f9b021d509874d98d033fdc171884f41e1c06efe6d6739e736`  
		Last Modified: Mon, 08 Dec 2025 22:39:53 GMT  
		Size: 87.0 MB (86986024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aac1d3794d4bc0de1ea1c3e6b3ed7fa48539c6db503563d326d34289a36dad86`  
		Last Modified: Mon, 08 Dec 2025 22:39:46 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:bc510da5afd7ec5a50b651c2e23672e242ab781e16ff5794d8c67c7de679e847
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7516549 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:872d8eacc7b17aa3ce26b673b7c19873e526aa1cf577e8e0fc25c253fdb1d91a`

```dockerfile
```

-	Layers:
	-	`sha256:71b9ee0b69cf729863b02881b3473a020a98d91ccc43bb88221448bb6d47ee05`  
		Last Modified: Tue, 09 Dec 2025 01:40:36 GMT  
		Size: 7.5 MB (7502307 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cdff75e5ccd8f6a414501b4d5f506874c5dc95e1fb68f4c7a4be70e7138b1424`  
		Last Modified: Tue, 09 Dec 2025 01:40:37 GMT  
		Size: 14.2 KB (14242 bytes)  
		MIME: application/vnd.in-toto+json
