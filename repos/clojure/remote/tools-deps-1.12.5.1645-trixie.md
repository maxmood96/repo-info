## `clojure:tools-deps-1.12.5.1645-trixie`

```console
$ docker pull clojure@sha256:6cec1990e9a2b00be5087f85a99cf274429651806ce5c6abff4524c7fc4970e1
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

### `clojure:tools-deps-1.12.5.1645-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:4dff565d5cdbd9433bd52ec4a33f17f515231a5eea84f720b80ca2c98a669b4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.5 MB (227493781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8578b76b239fe661876eb6a95c477de144101ccf0521c679cf3ff8b8cc914be7`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1779062400'
# Wed, 20 May 2026 00:01:42 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 20 May 2026 00:01:42 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 20 May 2026 00:01:42 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 May 2026 00:01:42 GMT
ENV CLOJURE_VERSION=1.12.5.1645
# Wed, 20 May 2026 00:01:42 GMT
WORKDIR /tmp
# Wed, 20 May 2026 00:01:59 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "3d6e8428fd4c7f76de9f87f77b2347f293109f4e88fb20c154b3fa34a7f687dd *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 20 May 2026 00:01:59 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 20 May 2026 00:02:00 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 20 May 2026 00:02:00 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 20 May 2026 00:02:00 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:f32f49ce655a9cf7c1fd4ca1417ddb39a54cedf4b7ff35de20f8009c18dd7a96`  
		Last Modified: Tue, 19 May 2026 22:37:05 GMT  
		Size: 49.3 MB (49310623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51b8ea5147a5ada10c1e36dce6d8a3e665d639f45dfa06782da4a48f8e6a9d9e`  
		Last Modified: Wed, 20 May 2026 00:02:23 GMT  
		Size: 92.6 MB (92574574 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12acce1c40840ebc1b65fec797cdc776981552e04677e3dbae6be44e60f5f01e`  
		Last Modified: Wed, 20 May 2026 00:02:23 GMT  
		Size: 85.6 MB (85607542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cd6b53c58fa866c3620a8e725e6bed328578e76102ec2eafc9e9e49e4dac46d`  
		Last Modified: Wed, 20 May 2026 00:02:19 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf84b8bb7ceb1e74a9abb2f89e278e76c8819407894601e8afe010306ebea5ad`  
		Last Modified: Wed, 20 May 2026 00:02:19 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.12.5.1645-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:6608d2e7fc79932909ea4476107b72435bae3f9e51ef051dfea91c5ddfa35f6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7456127 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e609bb96e708853bb77cc0477fcbe48142dcfa7172f36bf41d14b1adff19d633`

```dockerfile
```

-	Layers:
	-	`sha256:6d64610521ecbf92e7904d344f89f5864ee4ad57ec20b00bb3ab8cfa3e00de57`  
		Last Modified: Wed, 20 May 2026 00:02:20 GMT  
		Size: 7.4 MB (7439558 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2089f57638ac3da13e459d56d85d61a58c8bc6d643bec5cc80d1551e630e1c3c`  
		Last Modified: Wed, 20 May 2026 00:02:20 GMT  
		Size: 16.6 KB (16569 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-1.12.5.1645-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:3a2a2c3d8cda91c207635ff563d8287eba469509dc30c614997394126fcfdb76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.6 MB (226647338 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbb122b61eba2a7f8febf9a83e365600be743e179de72d4ee5f563be36409370`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1779062400'
# Wed, 20 May 2026 00:08:25 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 20 May 2026 00:08:25 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 20 May 2026 00:08:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 May 2026 00:08:25 GMT
ENV CLOJURE_VERSION=1.12.5.1645
# Wed, 20 May 2026 00:08:25 GMT
WORKDIR /tmp
# Wed, 20 May 2026 00:08:43 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "3d6e8428fd4c7f76de9f87f77b2347f293109f4e88fb20c154b3fa34a7f687dd *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 20 May 2026 00:08:43 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 20 May 2026 00:08:43 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 20 May 2026 00:08:43 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 20 May 2026 00:08:43 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:635135721e54f918d2d81497bc66b71f98aee3b440dd6498218827c56d7d277f`  
		Last Modified: Tue, 19 May 2026 22:37:01 GMT  
		Size: 49.7 MB (49672220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49ce3dd0057a2a2ec4a603eb373e747d6b9d1b79507268496f43627a5f7d237e`  
		Last Modified: Wed, 20 May 2026 00:08:58 GMT  
		Size: 91.5 MB (91542254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e52aa0ca6820ccd789b45aadfc7a68500f4768f048b341115caf9580d2a6402`  
		Last Modified: Wed, 20 May 2026 00:09:05 GMT  
		Size: 85.4 MB (85431819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39caff6453bbf9e0b6eadecc9995040ea3ec8f2e58ca7d681d562a052262fe31`  
		Last Modified: Wed, 20 May 2026 00:09:03 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b79c585a1ac46cd2873f9f44fcd1c427e343243a201393e7f9701269661e81f`  
		Last Modified: Wed, 20 May 2026 00:09:03 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.12.5.1645-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:2a90a7161e06c42e617edb1f14f6d09e4807e2c678407da696c18abe4a861b75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7462683 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bff132a935d8c0b9578630813e7688aee3bb9b0bf40c833c87bcac6fda0aa0b8`

```dockerfile
```

-	Layers:
	-	`sha256:d9e68802e20f92c2b208559ace9bbe890f6373a5d980c1066995641b7b422b25`  
		Last Modified: Wed, 20 May 2026 00:09:03 GMT  
		Size: 7.4 MB (7445972 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f0f2664f958173aad1e5d74c22ebc0e4cfeaab26c644fb94934785e87274c743`  
		Last Modified: Wed, 20 May 2026 00:09:03 GMT  
		Size: 16.7 KB (16711 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-1.12.5.1645-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:966eea2ce52b7221519a29182c12ddc823be9a07eff0082b486264543311f621
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.1 MB (236074019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e0c1edebc7a1374347926dfff06e386df7c0bc82fda2c1bcf2a59833bbe7d1e`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1779062400'
# Wed, 20 May 2026 06:05:58 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 20 May 2026 06:05:58 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 20 May 2026 06:05:58 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 May 2026 06:05:58 GMT
ENV CLOJURE_VERSION=1.12.5.1645
# Wed, 20 May 2026 06:05:59 GMT
WORKDIR /tmp
# Wed, 20 May 2026 06:09:25 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "3d6e8428fd4c7f76de9f87f77b2347f293109f4e88fb20c154b3fa34a7f687dd *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 20 May 2026 06:09:25 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 20 May 2026 06:09:26 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 20 May 2026 06:09:26 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 20 May 2026 06:09:26 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:55497c62a793e62a2e78a3fd85fcedf060da73e331ad107733199ea991106b96`  
		Last Modified: Tue, 19 May 2026 22:37:59 GMT  
		Size: 53.1 MB (53132182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ec19a238e74deea8797932477dbefdee56677e4d3a52ffe0c521942846410b8`  
		Last Modified: Wed, 20 May 2026 06:07:13 GMT  
		Size: 91.9 MB (91914019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:282fd401727ed792c946ad34b4a5d493109fe4f7089ec66ec8d96065edc37078`  
		Last Modified: Wed, 20 May 2026 06:10:02 GMT  
		Size: 91.0 MB (91026772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9aa107020efe88a0128029d667d4bf47da95cd01c6fa99ad6b8fce95e69c0a7e`  
		Last Modified: Wed, 20 May 2026 06:10:00 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfb381bc353f4351f87664bc82cbc4c10c5deee0b10115355af339b4d6d7bc8b`  
		Last Modified: Wed, 20 May 2026 06:09:59 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.12.5.1645-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:ee4032530291ed7fa145274f75a9d70ff1ad8c37467a5c2ed63291fb3b298684
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7443932 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16c20df8dac0293ead9bf1ef0bde044d0d74f4454327fd485a2cacfb8f031379`

```dockerfile
```

-	Layers:
	-	`sha256:a0579f24341503d865099d1a6f27e24e78923d78ca660777a50a6cd24e132f2d`  
		Last Modified: Wed, 20 May 2026 06:10:00 GMT  
		Size: 7.4 MB (7427303 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6965eb62198842f9cd98cb28955810ac867bf2db2ba9c7176d909ae551021c91`  
		Last Modified: Wed, 20 May 2026 06:09:59 GMT  
		Size: 16.6 KB (16629 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-1.12.5.1645-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:b15642af59d8c8131f47082cb61f6766ff2adf7122059980541e69f977785095
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **224.4 MB (224391780 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a397e865a82c6091a0b0880af60d101656bfbd41b0a10cc6f3434303de4adcd`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1779062400'
# Wed, 20 May 2026 01:47:23 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 20 May 2026 01:47:23 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 20 May 2026 01:47:23 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 May 2026 01:47:23 GMT
ENV CLOJURE_VERSION=1.12.5.1645
# Wed, 20 May 2026 01:47:23 GMT
WORKDIR /tmp
# Wed, 20 May 2026 01:48:37 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "3d6e8428fd4c7f76de9f87f77b2347f293109f4e88fb20c154b3fa34a7f687dd *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 20 May 2026 01:48:37 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 20 May 2026 01:48:37 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 20 May 2026 01:48:37 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 20 May 2026 01:48:37 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:1540dbb0587ae9097c9d04c50809503aa74d42814940d640c6659645acc0bc6c`  
		Last Modified: Tue, 19 May 2026 22:37:00 GMT  
		Size: 49.4 MB (49379780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e77a591861f1b273c45555677bf026cf5bd1c028b177d75ed2f6b38f41fd6977`  
		Last Modified: Wed, 20 May 2026 01:48:03 GMT  
		Size: 88.4 MB (88420336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb35ff6ed81ed2db31e4bd8fed9f124ebd8d7e5c108c365411e07e51ce9a12d0`  
		Last Modified: Wed, 20 May 2026 01:49:02 GMT  
		Size: 86.6 MB (86590623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6538ece9e0a22a8e688e0c120ca3521f136fd3df876c66f753b956aedbb128c2`  
		Last Modified: Wed, 20 May 2026 01:49:01 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1fe09cada1f08de1ab1c676a58071d5e611a983fb4596b0a8fc4486a131b6f2`  
		Last Modified: Wed, 20 May 2026 01:49:01 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.12.5.1645-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:72a0e24c45e15920feb15976fd2c53b8000af0f857814b5b338422c524b98f79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7436610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e55e93a7cf529e1c4aa2736b6a2ca3442d77bd2ee4be1a4d281ffd455d63a4d`

```dockerfile
```

-	Layers:
	-	`sha256:0347178f97c8e7cb7931b1aed2f3350fdca72fb18afbf23b893bffd908e8e4c6`  
		Last Modified: Wed, 20 May 2026 01:49:01 GMT  
		Size: 7.4 MB (7420042 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0930ed16bbf9afcdd913a6d6eb445fa331da2cf26d876070bcd7e3d94b235fb9`  
		Last Modified: Wed, 20 May 2026 01:49:01 GMT  
		Size: 16.6 KB (16568 bytes)  
		MIME: application/vnd.in-toto+json
