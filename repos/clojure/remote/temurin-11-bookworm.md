## `clojure:temurin-11-bookworm`

```console
$ docker pull clojure@sha256:61b29b85fb7d79a16ad676ddd234f8f6680062995caaa509d00447f5c2929812
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

### `clojure:temurin-11-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:55cc9fe5d758e53fad5f6d088ad1b7aa9c8d2e5875856509baf61b3dae22b432
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.6 MB (275594910 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f8da4e75134f6d40988b01fbe17ef1916922a033b836a6851b097890c92e1af`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1779062400'
# Tue, 19 May 2026 23:57:44 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 19 May 2026 23:57:44 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 19 May 2026 23:57:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 May 2026 23:57:44 GMT
ENV CLOJURE_VERSION=1.12.5.1645
# Tue, 19 May 2026 23:57:44 GMT
WORKDIR /tmp
# Tue, 19 May 2026 23:57:58 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "3d6e8428fd4c7f76de9f87f77b2347f293109f4e88fb20c154b3fa34a7f687dd *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 19 May 2026 23:57:58 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 19 May 2026 23:57:58 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:4887723d153cfd7fd9e356c8730311c36a64e4f9329f9d3ae1929e05715f2e73`  
		Last Modified: Tue, 19 May 2026 22:36:12 GMT  
		Size: 48.5 MB (48495432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ddc012571f61fa41d0a52f1f62c383cc0a2f77ddeca4013c3d2a35bf9048035`  
		Last Modified: Tue, 19 May 2026 23:58:21 GMT  
		Size: 145.9 MB (145886244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afbd317a585769aba59867cd625bcc00debc5cd5ffbff77a667441db857782bd`  
		Last Modified: Tue, 19 May 2026 23:58:20 GMT  
		Size: 81.2 MB (81212589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cee941ae0c4a5a5a66562dac64af1cf75f52c7b66d72b03cb9b58ec4eaefc7c`  
		Last Modified: Tue, 19 May 2026 23:58:16 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:1b2cc7bb6a7947912a72e7876ea561a109e4195e8db8a43e79931b72aea0721c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7412828 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5268f2eec8a9b588639062b6d060d1a070a8c55d5d235ebeca89dce135bfaf55`

```dockerfile
```

-	Layers:
	-	`sha256:cd52795fa07811f42083c171ad0891f00d9e75a4f56446a93be0d686b0925a3b`  
		Last Modified: Tue, 19 May 2026 23:58:17 GMT  
		Size: 7.4 MB (7398465 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d0b3b1cc9494f090797326c2b2f5e1232744a0a030af596bb1812e7574199cd9`  
		Last Modified: Tue, 19 May 2026 23:58:17 GMT  
		Size: 14.4 KB (14363 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:c090e6ec8a184b4a194aa7c11c60b95e605209ac771dbed947e6d43a0ed56c69
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.2 MB (272175940 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd91325c9ce57537115a8bb98f913031d660649c95407c841aa7f9e64b1761a7`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1779062400'
# Wed, 20 May 2026 00:04:55 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 20 May 2026 00:04:55 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 20 May 2026 00:04:55 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 May 2026 00:04:55 GMT
ENV CLOJURE_VERSION=1.12.5.1645
# Wed, 20 May 2026 00:04:55 GMT
WORKDIR /tmp
# Wed, 20 May 2026 00:05:10 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "3d6e8428fd4c7f76de9f87f77b2347f293109f4e88fb20c154b3fa34a7f687dd *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 20 May 2026 00:05:10 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 20 May 2026 00:05:10 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:1fbcdab7270278c1f989ae72190255d85d2117e990efb76cde6eb206b803672c`  
		Last Modified: Tue, 19 May 2026 22:36:02 GMT  
		Size: 48.4 MB (48379432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:861bd818b5984d27ca5b509953d8b641bd703eef5a674e6eb554d94c5b04673c`  
		Last Modified: Wed, 20 May 2026 00:05:32 GMT  
		Size: 142.6 MB (142582234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:412ef044bcd69167eb7f182b2ae9820d21bf8fade27dbf8010600c6969a41515`  
		Last Modified: Wed, 20 May 2026 00:05:31 GMT  
		Size: 81.2 MB (81213629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18cc0065d71328eaf6df5915e922d3dccaa3b27652bbf4f0beeaf3120116bdee`  
		Last Modified: Wed, 20 May 2026 00:05:28 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:5d1220fa1c1ece32e403f6e69c72e2698d1b2adf2d441cf53fb5941a6abda2d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7419326 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c62a109c557b256ca2081a951769d867a35c63d0e4d20e64e6a0d1229093d51a`

```dockerfile
```

-	Layers:
	-	`sha256:d11a65e599a7fdfc4b70f58da01d8c894e753e839620063c0809b919aa073867`  
		Last Modified: Wed, 20 May 2026 00:05:28 GMT  
		Size: 7.4 MB (7404846 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:30c5b43f448acebd44baf3414d7566015b3ffe1a91ff57a24117e2d84513a8ba`  
		Last Modified: Wed, 20 May 2026 00:05:28 GMT  
		Size: 14.5 KB (14480 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-bookworm` - linux; ppc64le

```console
$ docker pull clojure@sha256:6ad2315bde3e9d9072f76720ca146a3970eed1146dbd04e5a87840086a16c130
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.5 MB (272497718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:847956d6385ac57556682543850d095e420f3406ae4ec9a4ab89e7ff74dbe2dc`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1779062400'
# Wed, 20 May 2026 05:48:21 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 20 May 2026 05:48:21 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 20 May 2026 05:48:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 May 2026 05:48:21 GMT
ENV CLOJURE_VERSION=1.12.5.1645
# Wed, 20 May 2026 05:48:21 GMT
WORKDIR /tmp
# Wed, 20 May 2026 05:52:00 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "3d6e8428fd4c7f76de9f87f77b2347f293109f4e88fb20c154b3fa34a7f687dd *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 20 May 2026 05:52:01 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 20 May 2026 05:52:01 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:b3943e183051423c3dc79fa53ad6d50fff9621945bbfc636eec039b14ead2b66`  
		Last Modified: Tue, 19 May 2026 22:35:10 GMT  
		Size: 52.3 MB (52340199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:364f207e22b4bc1386011d3dcfe728278cc7f25d3c798c746cd6f1f56efcde80`  
		Last Modified: Wed, 20 May 2026 05:49:33 GMT  
		Size: 133.1 MB (133110125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e741b6f8ba7fb4e9a9894bbf089b50da27537107a79aac5dda24767297836c5`  
		Last Modified: Wed, 20 May 2026 05:52:38 GMT  
		Size: 87.0 MB (87046749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64ce021c76eabc12145576c11a4adc435a911ba0f458a36ba51d17605ed1226a`  
		Last Modified: Wed, 20 May 2026 05:52:33 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:0c9231ac6e0ae573df90a33c1922aa44dc1436a48ad9c002b93c4a740f063296
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7416522 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68e81a69dd7b545edb1d8513bb1529f304d4693831a2ea3a5cdef1c720019af6`

```dockerfile
```

-	Layers:
	-	`sha256:6a27542fcd0450c298147e1eca06feccb6c2980137323f896d56f85493243665`  
		Last Modified: Wed, 20 May 2026 05:52:36 GMT  
		Size: 7.4 MB (7403066 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:db981124b9695da2aea4d4664fb50de89849fc9ccba84a0a2bc85d930ce9e966`  
		Last Modified: Wed, 20 May 2026 05:52:35 GMT  
		Size: 13.5 KB (13456 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-bookworm` - linux; s390x

```console
$ docker pull clojure@sha256:3c7b2874d407589008e6e23dce260ac4ae7c199352a1542636ce4f1cdc9838db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.8 MB (253833924 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:118bddc4b114c1112de8f3ea478d0233be416ee31724fbc992ec2554ceb8ecec`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1779062400'
# Wed, 20 May 2026 01:41:32 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 20 May 2026 01:41:32 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 20 May 2026 01:41:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 May 2026 01:41:32 GMT
ENV CLOJURE_VERSION=1.12.5.1645
# Wed, 20 May 2026 01:41:32 GMT
WORKDIR /tmp
# Wed, 20 May 2026 01:42:44 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "3d6e8428fd4c7f76de9f87f77b2347f293109f4e88fb20c154b3fa34a7f687dd *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 20 May 2026 01:42:44 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 20 May 2026 01:42:44 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:e0fc2c7a6bb12f7a9b333cc117b6ea5fa5cf251c5fa4dd298303beee01028f59`  
		Last Modified: Tue, 19 May 2026 22:35:39 GMT  
		Size: 47.2 MB (47155589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d517d3699a232ef2589d952b25b33f3580fd7988f3a577091e4faec6269c9289`  
		Last Modified: Wed, 20 May 2026 01:42:11 GMT  
		Size: 126.7 MB (126651734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d31a604dc8ab8f932b68a89db39d068e25c841ef5bdc344638eebc3a40376692`  
		Last Modified: Wed, 20 May 2026 01:43:09 GMT  
		Size: 80.0 MB (80025955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47cf112661cd85a023cb509c923d68773cb10e3a2e4464358bbea7bc3f1aeb3b`  
		Last Modified: Wed, 20 May 2026 01:43:07 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:23a2867f97455501caec70c48cb510a807f7f8ebbb4c6208a7836e77dea3194e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7404151 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e1fb2f7168e1ca4b380a51e2548be0f086dd437a9fc8e949ec408d50f77dbda`

```dockerfile
```

-	Layers:
	-	`sha256:b708ecb7631d377b9fd710cb8dfac787c43d9307785e553f877675a1e8812866`  
		Last Modified: Wed, 20 May 2026 01:43:07 GMT  
		Size: 7.4 MB (7389788 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f9d1d2baf2868b36c28a1b96ca88685e87cfec60c932698ab84312da4f56f7bb`  
		Last Modified: Wed, 20 May 2026 01:43:07 GMT  
		Size: 14.4 KB (14363 bytes)  
		MIME: application/vnd.in-toto+json
