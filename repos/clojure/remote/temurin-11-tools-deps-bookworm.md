## `clojure:temurin-11-tools-deps-bookworm`

```console
$ docker pull clojure@sha256:cdb9afce7cd969a91187b408e3b908105f339fd5c2f210446ac31c0d9fea01d8
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

### `clojure:temurin-11-tools-deps-bookworm` - linux; amd64

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

### `clojure:temurin-11-tools-deps-bookworm` - unknown; unknown

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

### `clojure:temurin-11-tools-deps-bookworm` - linux; arm64 variant v8

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

### `clojure:temurin-11-tools-deps-bookworm` - unknown; unknown

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

### `clojure:temurin-11-tools-deps-bookworm` - linux; ppc64le

```console
$ docker pull clojure@sha256:ad71579b0a39252fa9d465664cfebd33b256ca1947be05aca60dc1bc5fa32a75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.5 MB (272480967 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfb616e69751cf88e8ca13e4f6def5a8db909dcad24cb776ace4b4543f0b94cf`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1777939200'
# Sat, 09 May 2026 02:25:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 09 May 2026 02:25:03 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 09 May 2026 02:25:03 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 09 May 2026 02:25:03 GMT
ENV CLOJURE_VERSION=1.12.5.1645
# Sat, 09 May 2026 02:25:03 GMT
WORKDIR /tmp
# Fri, 15 May 2026 20:17:50 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "3d6e8428fd4c7f76de9f87f77b2347f293109f4e88fb20c154b3fa34a7f687dd *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 15 May 2026 20:17:50 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 15 May 2026 20:17:50 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:30ef9f53c997c6c1f1ab8f4cc559b32d9206d169c54ad5a0f0363076708fffef`  
		Last Modified: Fri, 08 May 2026 19:44:07 GMT  
		Size: 52.3 MB (52336787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07cbaabc187f4e33faa4937073e6b8d37c4b4ee8836b24edba986c27660880f2`  
		Last Modified: Sat, 09 May 2026 02:26:07 GMT  
		Size: 133.1 MB (133110168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfb2b6d4d875c4b9e472651f2ac7937e0f343a7c36537581ea54dcbf08d0638e`  
		Last Modified: Fri, 15 May 2026 20:18:29 GMT  
		Size: 87.0 MB (87033365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:243527edf726bd337d3bbf0233e9ee9b4c1220f99f67d2358812d118d471d896`  
		Last Modified: Fri, 15 May 2026 20:18:26 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:c9c3a5e6a90174ee7b17434b3b1cc430ab72f45ae881419420b302f319da73a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7416500 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e012574e247da8b3c66fe94c0deba7c9e993338c012a7e88a2bac03d2d9266f8`

```dockerfile
```

-	Layers:
	-	`sha256:5c80bfc9b27ba86312fe2be2838b7cc83f5035bdf233043490ad5ea2cf6fb19d`  
		Last Modified: Fri, 15 May 2026 20:18:27 GMT  
		Size: 7.4 MB (7403044 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d48ec215bd4a75123942f9ee58130a6a8e840ca18d4ddc4d70bdaf7bbe7690d9`  
		Last Modified: Fri, 15 May 2026 20:18:26 GMT  
		Size: 13.5 KB (13456 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-bookworm` - linux; s390x

```console
$ docker pull clojure@sha256:fe4d8373ad1b5a128fd7da96954db805d6807832fcb192561821dec84b74894c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.8 MB (253825767 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:284c1087f036282200555891a05963f386f8b7e363f1d2264b7bdee1f28cd811`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1777939200'
# Thu, 14 May 2026 23:32:15 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 14 May 2026 23:32:15 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 14 May 2026 23:32:15 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 14 May 2026 23:32:15 GMT
ENV CLOJURE_VERSION=1.12.5.1645
# Thu, 14 May 2026 23:32:15 GMT
WORKDIR /tmp
# Fri, 15 May 2026 20:13:35 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "3d6e8428fd4c7f76de9f87f77b2347f293109f4e88fb20c154b3fa34a7f687dd *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 15 May 2026 20:13:36 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 15 May 2026 20:13:36 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:124dbe049873037f973f01d877ec004bf4cd3ce5723d0b8f2067c58ad98137d6`  
		Last Modified: Fri, 08 May 2026 18:27:29 GMT  
		Size: 47.1 MB (47148023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e52372d5fb2e4448599149f5fdd18e1d6933ee7757f50701f6b69d3caa03696a`  
		Last Modified: Thu, 14 May 2026 23:33:05 GMT  
		Size: 126.7 MB (126651718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9321ceea7ad7f84a7e5a6ae84c96b339fc1997ccca2d9b23774cdf1dce56bcb7`  
		Last Modified: Fri, 15 May 2026 20:14:17 GMT  
		Size: 80.0 MB (80025378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7264922cb08a03539a1a09b3ce8dcb79e62402cfa2033a0a48b49efc5ef33cc9`  
		Last Modified: Fri, 15 May 2026 20:14:09 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:df9b4811c519a6aa91882687af8f43c141b62393abc1c3b4331291982c656ff1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7403174 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf4b28584aad5800a1c1c71adced07e47b44a6bfeda7d8047eacb9d63cd4b28f`

```dockerfile
```

-	Layers:
	-	`sha256:8e994ce011c7348eae3685edb66cbd83e92bca2afcc2e771a80063b7c75589ca`  
		Last Modified: Fri, 15 May 2026 20:14:14 GMT  
		Size: 7.4 MB (7389766 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:299cc4c22b150a6dab2a076d8ace9c3bd480dded54e97e2c8e8940a43043269d`  
		Last Modified: Fri, 15 May 2026 20:14:13 GMT  
		Size: 13.4 KB (13408 bytes)  
		MIME: application/vnd.in-toto+json
