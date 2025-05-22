## `clojure:temurin-21-tools-deps-1.12.0.1530-bookworm-slim`

```console
$ docker pull clojure@sha256:d88b0b7ef4dcd4b8088d234ef212da1bcc4a2b629b7c6e0e4539b7cd8f2b61f4
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

### `clojure:temurin-21-tools-deps-1.12.0.1530-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:f55aeab776702033c5409f7d8ca262e8cbafc1f15c9c901a0a18e1561b68ced4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.4 MB (255391809 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f80b5dc6732a16a16287555cbe73fe60b883948aa558263f5f9cdb80394a8f93`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 13 May 2025 03:53:36 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1747699200'
# Tue, 13 May 2025 03:53:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 May 2025 03:53:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 May 2025 03:53:36 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Tue, 13 May 2025 03:53:36 GMT
WORKDIR /tmp
# Tue, 13 May 2025 03:53:36 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 May 2025 03:53:36 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:61320b01ae5e0798393ef25f2dc72faf43703e60ba089b07d7170acbabbf8f62`  
		Last Modified: Wed, 21 May 2025 22:27:39 GMT  
		Size: 28.2 MB (28225330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8542d4e770794958538ba57486be8774fb5f96813bec247cec4c977cc9f8cc44`  
		Last Modified: Wed, 21 May 2025 23:33:30 GMT  
		Size: 157.6 MB (157634499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d3c0b4cb45a2b0080a2fdd3d3bc03d0dcc2469ef18099b15f16d6ffa88e9ac1`  
		Last Modified: Wed, 21 May 2025 23:33:29 GMT  
		Size: 69.5 MB (69530939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b169f613a379ada501d3bf07740ec349604bed61b145a3db14f65b310e7920ac`  
		Last Modified: Wed, 21 May 2025 23:33:28 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0518364691994b9cf3bb2d59aae901fe123f76dac8cf97a4dfdfdf0f7e07f7a0`  
		Last Modified: Wed, 21 May 2025 23:33:28 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.0.1530-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:69024aea5914573ac00c4c7f59160ff8d4bb7fba50bc77641befe111405652ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4981871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:323f5479b6691cbdd9ec979e808d69e77502babf7a8e3d33ca644108da0b8d28`

```dockerfile
```

-	Layers:
	-	`sha256:65aa8f2522e9d01286ed6cdcfb04ef80a2aceabad6819bbbf67ee3d0122c24f5`  
		Last Modified: Wed, 21 May 2025 23:33:28 GMT  
		Size: 5.0 MB (4965296 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:77ec3819f9703816c6c8be10d39fed76163226fee39e67646faa344ad84c7227`  
		Last Modified: Wed, 21 May 2025 23:33:28 GMT  
		Size: 16.6 KB (16575 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-1.12.0.1530-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:472b3e992b251bc740b05576ed924ba8edf58f56dc6771b88945d8a48bebfc5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.4 MB (253381231 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92300a2cd98036729e9a37bed5aece528a32d674c112c38e5df0193b71268429`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 13 May 2025 03:53:36 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1747699200'
# Tue, 13 May 2025 03:53:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 May 2025 03:53:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 May 2025 03:53:36 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Tue, 13 May 2025 03:53:36 GMT
WORKDIR /tmp
# Tue, 13 May 2025 03:53:36 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 May 2025 03:53:36 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:b16f1b16678093d11ecfece1004207a40f9bc1b7d9d1d16a070c1db552038818`  
		Last Modified: Wed, 21 May 2025 22:27:55 GMT  
		Size: 28.1 MB (28065280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b920f2782e54c0936283f35994e494b7bf3269bc82c414f10cec27aba0c88c7c`  
		Last Modified: Thu, 22 May 2025 08:29:52 GMT  
		Size: 155.9 MB (155928808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2210aa8eba8f23b1aa674fa25a493b53439b03040502635f13fa431a7285ecd`  
		Last Modified: Thu, 22 May 2025 08:34:58 GMT  
		Size: 69.4 MB (69386103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d88593c1f56760164d0bdffced0a919b9c51fc03ef31749dc1b6add14896a6f1`  
		Last Modified: Thu, 22 May 2025 08:34:55 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e1847f5f11a81fd19c14e7acc7700802e8aed0ec770890eda2fa0f55d20ed3c`  
		Last Modified: Thu, 22 May 2025 08:34:56 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.0.1530-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:e6547270c39fe566b746bc6d76103a3a59dd83d2914d7c261b5141725c3bb36d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4987798 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f6bf3aad480487abcb20c7d0c84d0d4745321c7962f5f180db71ffd5cebbf71`

```dockerfile
```

-	Layers:
	-	`sha256:4a89cad8d47c1d0bb93cf7c00c780042c71c16da31c2affb9da9f32c4986fa5e`  
		Last Modified: Thu, 22 May 2025 08:34:56 GMT  
		Size: 5.0 MB (4971081 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bf8129d0f5e94352a063e88b8dc6da9df48d16e3e0d681f21d03d5ca49d725d6`  
		Last Modified: Thu, 22 May 2025 08:34:55 GMT  
		Size: 16.7 KB (16717 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-1.12.0.1530-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:870a4105570345d24fac35fb1ef6814935ab86aabefd60f96485a1741e1cfe92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **265.2 MB (265219191 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4911092a6ca837e9deae63c21cc4ccd5700e507dfc88c35a16b1d45518eb9f85`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1745798400'
# Tue, 13 May 2025 03:53:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 May 2025 03:53:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 May 2025 03:53:36 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Tue, 13 May 2025 03:53:36 GMT
WORKDIR /tmp
# Tue, 13 May 2025 03:53:36 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 May 2025 03:53:36 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:a53e75e229cd115b5249f6e60d40785f1bfff9e7ccc2df65672a6f67afd0e348`  
		Last Modified: Mon, 28 Apr 2025 21:22:04 GMT  
		Size: 32.1 MB (32068443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97c25f006c8da87634b15cd9ff02661544ef2e79e4d05effbd9011c7add02414`  
		Last Modified: Tue, 13 May 2025 19:11:46 GMT  
		Size: 157.8 MB (157804905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d9f36d96a1a1f25001324066e65ae78670ac3199847ee6e655f355e1bf729e1`  
		Last Modified: Tue, 13 May 2025 19:22:27 GMT  
		Size: 75.3 MB (75344800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5330057daac8d954d9c3dad23ffefe0d30e07fabad448cf31c7c05990005b3e`  
		Last Modified: Tue, 13 May 2025 19:22:24 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e095547b249d76a3118e38218c91d56eca41fd05b6f7a7c56a57b62ee192314e`  
		Last Modified: Tue, 13 May 2025 19:22:24 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.0.1530-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:80d4ba771aecc72e6267e368d4b79c987309e3f468c2efd9d08d5ada2bce79f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4939402 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06e48ab9887236d04d547adfdd49b5be4dc019db280d30b24f552cef791b7ffa`

```dockerfile
```

-	Layers:
	-	`sha256:c76f38ad5d36846e7d14004088b64b714b1dd46c711dc12ad2f866ef38919153`  
		Last Modified: Tue, 13 May 2025 19:22:24 GMT  
		Size: 4.9 MB (4922767 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eacec4f081095adb05c3b7b4440913cd2311124b8c5bfd471fd31e870d8ab176`  
		Last Modified: Tue, 13 May 2025 19:22:24 GMT  
		Size: 16.6 KB (16635 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-1.12.0.1530-bookworm-slim` - linux; s390x

```console
$ docker pull clojure@sha256:a9a330b1e619a08f108fb8d9c372c763f08a1b2d24b057428f0d2143c9cf2c35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.1 MB (242122068 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ac2565a6c64a0c6023f45274a0c845050521098048c6cb07584af60205bdf97`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 13 May 2025 03:53:36 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1747699200'
# Tue, 13 May 2025 03:53:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 May 2025 03:53:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 May 2025 03:53:36 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Tue, 13 May 2025 03:53:36 GMT
WORKDIR /tmp
# Tue, 13 May 2025 03:53:36 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 May 2025 03:53:36 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:fb6e196ef379785f6b759a20e90d74fe0566b240771695f724c27a44aa6cd3ce`  
		Last Modified: Wed, 21 May 2025 22:28:38 GMT  
		Size: 26.9 MB (26882808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d177fb8ec02d6978e79aaa55711654499f22bc1fcf2f8a5abc52b76abf19bcee`  
		Last Modified: Thu, 22 May 2025 03:58:13 GMT  
		Size: 146.9 MB (146910920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a13b2efab43c9edd8b305f51768c20be77c25f9545aaaa80115b609366988be`  
		Last Modified: Thu, 22 May 2025 04:02:34 GMT  
		Size: 68.3 MB (68327300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ab57f2307e98a9cd34dfd73025943166c9d52937b0a997b0c3fa6c2b7b378fc`  
		Last Modified: Thu, 22 May 2025 04:02:33 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b7762dd0bbe5b040acaae76f91c60bc639d49d14b52713d243c24d4fe3198d6`  
		Last Modified: Thu, 22 May 2025 04:02:33 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.0.1530-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:0a17cbecc85ba4292a05c2658ff6e352416f04fe08f897d6df782923d708c116
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4976084 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77d31842834735ff2f04eebd28d25893f4378066d368828a3d281eca5e6de2b9`

```dockerfile
```

-	Layers:
	-	`sha256:7715dc1ca9e113d0bcc03800a41643483c4a2d2343d2b6906feacb08ff731668`  
		Last Modified: Thu, 22 May 2025 04:02:33 GMT  
		Size: 5.0 MB (4959509 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:37ff184e21e26c27a8dadd5f97bd3274f4695918f8c813a3e6f17d49535354e5`  
		Last Modified: Thu, 22 May 2025 04:02:33 GMT  
		Size: 16.6 KB (16575 bytes)  
		MIME: application/vnd.in-toto+json
