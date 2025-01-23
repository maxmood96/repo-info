## `clojure:temurin-17-tools-deps-1.12.0.1495-bullseye`

```console
$ docker pull clojure@sha256:13377ece81420317dbaefc149c7911105dd907d4b7f4a8186a6c83d6f496caf8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-tools-deps-1.12.0.1495-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:f028b331f56ea362c52cc38c9c67bedf975cc6cb179453440dcc79183c3aee2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **267.5 MB (267455424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6735125ca4f6e77180adb84fec1ed63845326eac0169aac6e2d33e0cd4e863f`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 06 Jan 2025 23:07:46 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1736726400'
# Mon, 06 Jan 2025 23:07:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 06 Jan 2025 23:07:46 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 06 Jan 2025 23:07:46 GMT
ENV CLOJURE_VERSION=1.12.0.1495
# Mon, 06 Jan 2025 23:07:46 GMT
WORKDIR /tmp
# Mon, 06 Jan 2025 23:07:46 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8408034c095c531155acb08bef65ad1edf25f55226bb086dfaf0d0eee9cadd59 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 06 Jan 2025 23:07:46 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:de97e8062e06250e3c3cef0d40cfe62111bb4b74bcf6221e25a06452dacffcf6`  
		Last Modified: Tue, 14 Jan 2025 01:33:36 GMT  
		Size: 53.7 MB (53739164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94c0fd9204bb07d06c249dd4e836423788f666bbfe6980ecff000979906e8c1b`  
		Last Modified: Wed, 22 Jan 2025 19:37:00 GMT  
		Size: 144.5 MB (144536747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9571b0bde8969cf525ccb815529b2c67faf6ec6a74d3c85b45485a6a19ee49d`  
		Last Modified: Wed, 22 Jan 2025 19:37:00 GMT  
		Size: 69.2 MB (69178469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cac30e23f6ebeeb3738ee9d26670ca14302de6fe3eb6ff451a0152cb7f26338`  
		Last Modified: Wed, 22 Jan 2025 19:36:58 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe0b77c90a89d06adc6eab68606dfde315dfe6b8dca3db6d05f0ade49a4a0115`  
		Last Modified: Wed, 22 Jan 2025 19:36:58 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.0.1495-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:3f31cd7079af6d8d20ffea4d292db3835b27ae217ba97aed44262a76d6c91ccb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7220377 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc3b02b975d59a39c294be4d6eaf8b57132e3ab3bae79a2b981dc10497e0b984`

```dockerfile
```

-	Layers:
	-	`sha256:e7f645b2266f266d9f863704f644298aec8b2145b02d46c006539ec002ce37ce`  
		Last Modified: Wed, 22 Jan 2025 19:37:02 GMT  
		Size: 7.2 MB (7204557 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:05543cb6a2f436f15835ac1e2be43820d269383c5d0a815877d6c026fdbac220`  
		Last Modified: Wed, 22 Jan 2025 19:36:58 GMT  
		Size: 15.8 KB (15820 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.0.1495-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:37e2c4658e8f4f3eb0cdfef0c94a5db718ebe55eb63156e7e63b3fde5bba1fed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **264.9 MB (264912541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd333ea2df0b79256ee4904c4b340ae469bd0b8f5bcb9d16f127632d7ea31823`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 06 Jan 2025 23:07:46 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1736726400'
# Mon, 06 Jan 2025 23:07:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 06 Jan 2025 23:07:46 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 06 Jan 2025 23:07:46 GMT
ENV CLOJURE_VERSION=1.12.0.1495
# Mon, 06 Jan 2025 23:07:46 GMT
WORKDIR /tmp
# Mon, 06 Jan 2025 23:07:46 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8408034c095c531155acb08bef65ad1edf25f55226bb086dfaf0d0eee9cadd59 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 06 Jan 2025 23:07:46 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:1270858b2b9cb5d47abd119b946534b70ff7d09f29c425fc07b280e5c28971c6`  
		Last Modified: Tue, 14 Jan 2025 01:36:12 GMT  
		Size: 52.2 MB (52246060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2a83cadea50845dd03abea7a3d6efb27e951eb9e87f1d5e10c0e89572e38b27`  
		Last Modified: Thu, 23 Jan 2025 02:46:21 GMT  
		Size: 143.4 MB (143360991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2616c438d9e711a46199f8a19408bbb72bb8090d1266d3aa6812b0bcb90b494`  
		Last Modified: Thu, 23 Jan 2025 02:50:59 GMT  
		Size: 69.3 MB (69304448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df25089cb141aa0027619a5741e51ceb74199d26c3584c62b28698c42419c925`  
		Last Modified: Thu, 23 Jan 2025 02:50:57 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e71a46282f33a86a5107abba862f36095bf989a66b93635b0e3bbdc776233805`  
		Last Modified: Thu, 23 Jan 2025 02:50:57 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.0.1495-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:b1599514554497df0a76d58ec8ee6a59a456e75fa82ccfa1b91ffaf126b47505
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7225595 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52cdfffaed8f99bc778011ae12d138a42d5fd6b03b1a36f91c6638b061f3d63e`

```dockerfile
```

-	Layers:
	-	`sha256:7c7c126298eb4996a7a0d687fe4210418098c3a890f9be33f540eedb2b4b33e6`  
		Last Modified: Thu, 23 Jan 2025 02:50:57 GMT  
		Size: 7.2 MB (7209656 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:106711934a8c355de2dbc14496fb7c05bf4e2386878fedb2b3aaa9efee6bfb1f`  
		Last Modified: Thu, 23 Jan 2025 02:50:57 GMT  
		Size: 15.9 KB (15939 bytes)  
		MIME: application/vnd.in-toto+json
