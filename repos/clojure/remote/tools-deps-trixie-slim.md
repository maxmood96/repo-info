## `clojure:tools-deps-trixie-slim`

```console
$ docker pull clojure@sha256:6b01d97b817b1f2037d6711d3613327f71290e2f4d6c5ae3d1fe9cf1477f4e14
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

### `clojure:tools-deps-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:d492f6b9134b22c9fb7cb17fb47d30aa75a49717b010186225c94f98f38aac1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.3 MB (191307354 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6199dbcc1c99e4d2d64daa3934ccdb25c65966231447cd997c612c73cf7fb15`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1779062400'
# Thu, 04 Jun 2026 17:47:27 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 Jun 2026 17:47:27 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 04 Jun 2026 17:47:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Jun 2026 17:47:27 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Thu, 04 Jun 2026 17:47:27 GMT
WORKDIR /tmp
# Thu, 04 Jun 2026 17:47:44 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 04 Jun 2026 17:47:44 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 04 Jun 2026 17:47:44 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 04 Jun 2026 17:47:44 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 04 Jun 2026 17:47:44 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:5b4d6ff92fc4e14e911b7753c954fac965d48c40fe1075758d284148ccace970`  
		Last Modified: Tue, 19 May 2026 22:37:05 GMT  
		Size: 29.8 MB (29779926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:350fe9befa119b4116fe693fb88baf2ada42211da07b656c5961b19ee878ee9a`  
		Last Modified: Thu, 04 Jun 2026 17:48:06 GMT  
		Size: 92.6 MB (92574585 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93844fd46a46de3292a18000f90036735a439bf6b797c059592a3025e3943c73`  
		Last Modified: Thu, 04 Jun 2026 17:48:05 GMT  
		Size: 69.0 MB (68951803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b97df1c374c810440d6d022921016258a93eaee101a9238294f36d74c74bffa6`  
		Last Modified: Thu, 04 Jun 2026 17:48:01 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67658f8101f18d68b6caf6990e6c10f6802cf1341ac952e198c9e8a7fa16d3c3`  
		Last Modified: Thu, 04 Jun 2026 17:48:02 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:6f27ab4e73d64a101110f7876823614990c80a9804ff32ff400faba27de385d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5241969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6b84ff0ac5fcf2929982cd8fa1ef097735f9fcf510dd9c154528c39f7b61f3b`

```dockerfile
```

-	Layers:
	-	`sha256:2703410a4ad9c0ea4966fe7ba4485c3d55d305ef7633b149d05f37955359a32e`  
		Last Modified: Thu, 04 Jun 2026 17:48:02 GMT  
		Size: 5.2 MB (5225324 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0148f076b6c896f9a95c4ce63b192a8a48a4e15afd2da445ed7e8638d913ceae`  
		Last Modified: Thu, 04 Jun 2026 17:48:01 GMT  
		Size: 16.6 KB (16645 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:d638008a562313354e6117179a0c874cd4ecfc6dc85ae35fba70aa98aaf50fe6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **190.5 MB (190462551 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6303b38e6447c7f9f1947154dfec235a04a0365d508271fa64dd9ca0db8c71c4`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1779062400'
# Thu, 04 Jun 2026 17:47:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 Jun 2026 17:47:26 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 04 Jun 2026 17:47:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Jun 2026 17:47:26 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Thu, 04 Jun 2026 17:47:26 GMT
WORKDIR /tmp
# Thu, 04 Jun 2026 17:47:44 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 04 Jun 2026 17:47:44 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 04 Jun 2026 17:47:44 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 04 Jun 2026 17:47:44 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 04 Jun 2026 17:47:44 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:cda3d70ae7d7c3d0b3b57a99a2085f9d93e919a846913dc6517a420b348c123d`  
		Last Modified: Tue, 19 May 2026 22:36:58 GMT  
		Size: 30.1 MB (30141919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7116e817da7b8bfa45c840a9da6daeb6018af6aae8209cbab936a7f50ff13eef`  
		Last Modified: Thu, 04 Jun 2026 17:48:05 GMT  
		Size: 91.5 MB (91542254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79890f11d1295c20fb84ca72fec3521fbb7d7d718964661860f042e45945f882`  
		Last Modified: Thu, 04 Jun 2026 17:48:04 GMT  
		Size: 68.8 MB (68777338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c0e43356c4957d07148f077b4860fc3adeb777bb7ab51145cd662d8207147c9`  
		Last Modified: Thu, 04 Jun 2026 17:48:02 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e3d89b0be892483c926f5929f398dabbfa6044117f77fd82208b88c213f44f3`  
		Last Modified: Thu, 04 Jun 2026 17:48:02 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:5c753f8f7c2b61da12e0ce1911f2f4a21dea7facf087cc388d9c164bb1ef6203
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5247895 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:979a9c0c6f0a65b6416e37683ef12a5e097877ddf778053ab13d5a67670f70e7`

```dockerfile
```

-	Layers:
	-	`sha256:c4938453393344e12aff890939b97663b23c8edbef6a4bc23ee7977751c3ebc0`  
		Last Modified: Thu, 04 Jun 2026 17:48:02 GMT  
		Size: 5.2 MB (5231106 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:75d0b5bb1c44988a97da783814ec2ab73c90f3fd0d91b79023fa9ca94b396cf5`  
		Last Modified: Thu, 04 Jun 2026 17:48:02 GMT  
		Size: 16.8 KB (16789 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:b9f3377d9252bc1f7e9299108913471048276587aa4261dfc3b1473d6a61ef21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **199.9 MB (199884519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:436ffe2f2c10a4591721a6d4414bbe40a1e150da2ee1c6c64c070f3084900c0c`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1779062400'
# Thu, 04 Jun 2026 18:07:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 Jun 2026 18:07:57 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 04 Jun 2026 18:07:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Jun 2026 18:07:57 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Thu, 04 Jun 2026 18:07:57 GMT
WORKDIR /tmp
# Thu, 04 Jun 2026 18:08:43 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 04 Jun 2026 18:08:45 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 04 Jun 2026 18:08:46 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 04 Jun 2026 18:08:46 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 04 Jun 2026 18:08:46 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:4dea3595b4b879a8f487420dc7e601b4fe79f2769fed7f891c99b52fea019c27`  
		Last Modified: Tue, 19 May 2026 22:37:58 GMT  
		Size: 33.6 MB (33600453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:182d622beec6c4387449420f7de969ccad2b0cf20d00ff972fd1e3f0e33a65e8`  
		Last Modified: Thu, 04 Jun 2026 18:09:30 GMT  
		Size: 91.9 MB (91914038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0778cec8ae24ac85c06b6eddf4eb93507f3323644c73533d352c489337c88607`  
		Last Modified: Thu, 04 Jun 2026 18:09:30 GMT  
		Size: 74.4 MB (74368984 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f241c7541816eae6f16485ba845915b87ff4d38a943c6396034a157c8925b6f3`  
		Last Modified: Thu, 04 Jun 2026 18:09:26 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd76ead74be20ee7b20a3bc8ca92c53a439feb85ee30674f3a54f54979483780`  
		Last Modified: Thu, 04 Jun 2026 18:09:26 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:797941ed824b614be4bc47aef08949ffefbace0c2d705860945cf2fc1c4f389c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5229726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1ab5b2f3d563b88b7977060a7cda0c69f43ccc165b07cd70ba3d778807586e5`

```dockerfile
```

-	Layers:
	-	`sha256:882ce7216d02789e582de90a808f88d5d6d800fa014e3d4713003bc54b6867b0`  
		Last Modified: Thu, 04 Jun 2026 18:09:27 GMT  
		Size: 5.2 MB (5213019 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3b39d04d772def1461c1468a0289fcfd366c41ca936971e5fb3cc51bd63c7e17`  
		Last Modified: Thu, 04 Jun 2026 18:09:26 GMT  
		Size: 16.7 KB (16707 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:e60ba134c65cb8a5ba91d7de8f3d4f3a4325b303217d2fd91781d82960e0047f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.2 MB (188199656 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cdd18a4609b230d27fb39e0dca485c36924c324ae10229a1b957a93e59d2a41`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1779062400'
# Thu, 04 Jun 2026 17:46:27 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 Jun 2026 17:46:27 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 04 Jun 2026 17:46:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Jun 2026 17:46:27 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Thu, 04 Jun 2026 17:46:27 GMT
WORKDIR /tmp
# Thu, 04 Jun 2026 17:46:45 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 04 Jun 2026 17:46:45 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 04 Jun 2026 17:46:45 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 04 Jun 2026 17:46:45 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 04 Jun 2026 17:46:45 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:3a7bf300ab749fc8aaa5ec872160f889b9f1fd11db31bb5e8fe4d9ec131347b0`  
		Last Modified: Tue, 19 May 2026 22:36:59 GMT  
		Size: 29.8 MB (29845924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8cb2abef97cab031a8a03eae9742d83772b94def3b67a9c980af88c3a24ed49`  
		Last Modified: Thu, 04 Jun 2026 17:47:15 GMT  
		Size: 88.4 MB (88420320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ae26169630c9f2bde4bb360060930e6a1493813c57b7d7c92b2f3d621dbb32b`  
		Last Modified: Thu, 04 Jun 2026 17:47:13 GMT  
		Size: 69.9 MB (69932366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e66b636708cf29725d9886a98695a916258cbbcef27283bde218c432005932ed`  
		Last Modified: Thu, 04 Jun 2026 17:47:11 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72dea5a70f7d85493e97eaaf882c47c420a9967614bf51afab391500323368f7`  
		Last Modified: Thu, 04 Jun 2026 17:47:11 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:8f80e82b62efad334c190bacecb6995ce33ab5fac12b2664948e60c71d3747db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5222457 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d548cd1ce55d322a580e355b4012a4cb196ff7f7b8e0727ffa53132dcb90a796`

```dockerfile
```

-	Layers:
	-	`sha256:8657deb469c83f1fce1bd945fb43ceebe223854d07fb0aa1035039ff56385254`  
		Last Modified: Thu, 04 Jun 2026 17:47:11 GMT  
		Size: 5.2 MB (5205810 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:11d68846d9577217e87b2d5f28eb962ed3aa5af2207b4186f4cb44c5da16a24d`  
		Last Modified: Thu, 04 Jun 2026 17:47:11 GMT  
		Size: 16.6 KB (16647 bytes)  
		MIME: application/vnd.in-toto+json
