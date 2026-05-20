## `clojure:temurin-17-bookworm`

```console
$ docker pull clojure@sha256:99e3e3c386ea6242bda723fcc634587b40feebc7cc6b0beb9ea23371ed677500
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

### `clojure:temurin-17-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:5d0d9aa5c5a4bed2028bf9ba0eb1f6a3ba527ad1f386a9ce6fe77566b33fb544
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.6 MB (275613759 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e5e3abbb155cb4e3865938b002b6b1eee31f12319576046c017b5f57ac5fbd9`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1779062400'
# Tue, 19 May 2026 23:58:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 19 May 2026 23:58:46 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 19 May 2026 23:58:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 May 2026 23:58:46 GMT
ENV CLOJURE_VERSION=1.12.5.1645
# Tue, 19 May 2026 23:58:46 GMT
WORKDIR /tmp
# Tue, 19 May 2026 23:59:00 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "3d6e8428fd4c7f76de9f87f77b2347f293109f4e88fb20c154b3fa34a7f687dd *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 19 May 2026 23:59:00 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 19 May 2026 23:59:00 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 19 May 2026 23:59:00 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 19 May 2026 23:59:00 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:4887723d153cfd7fd9e356c8730311c36a64e4f9329f9d3ae1929e05715f2e73`  
		Last Modified: Tue, 19 May 2026 22:36:12 GMT  
		Size: 48.5 MB (48495432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe9b67e9c0efb882db9f67a1269b3b2939d472322b22a0f5e4a882f3b5a5eb29`  
		Last Modified: Tue, 19 May 2026 23:59:22 GMT  
		Size: 145.9 MB (145905476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d39be79db169aa082db3e99610108d12eb52d81003f242ce68ca8f822e94879`  
		Last Modified: Tue, 19 May 2026 23:59:21 GMT  
		Size: 81.2 MB (81211808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3370db1de17682bd9be2d6cbab6920b8b6e7aba2817a5b32ba822a8e38a758ec`  
		Last Modified: Tue, 19 May 2026 23:59:17 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edd50204ca88113286a8f9c1c77b0415d34db53247ed6c48a92009a72a3cb520`  
		Last Modified: Tue, 19 May 2026 23:59:17 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:9a48971ee56258fb0bae2a8224ff2d2f84355a68352eb1eab438c2eb1891ae02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7394879 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5df695862f3ded71f0f1cb4f8a0316ceb89d1804e97443b727e34f8ee9fbd198`

```dockerfile
```

-	Layers:
	-	`sha256:6958c4b73326ccf3f66784a78ddaa3db5c6631924513077827b82c8d5e630d91`  
		Last Modified: Tue, 19 May 2026 23:59:18 GMT  
		Size: 7.4 MB (7378949 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:beceb8d3f640b5afed04a8932f5459db1b2a02dde4621a8ab4a8b4643b3d8669`  
		Last Modified: Tue, 19 May 2026 23:59:17 GMT  
		Size: 15.9 KB (15930 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:2638c3b4ba176be7b31df1e93dd66a5f779557262bec6e965707afc6c675ff56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.3 MB (274318456 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff48184d5b0b935886f6ab9e4db3adb6fafcc335dc96341f40d9dca293feac41`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1779062400'
# Wed, 20 May 2026 00:05:53 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 20 May 2026 00:05:53 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 20 May 2026 00:05:53 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 May 2026 00:05:53 GMT
ENV CLOJURE_VERSION=1.12.5.1645
# Wed, 20 May 2026 00:05:53 GMT
WORKDIR /tmp
# Wed, 20 May 2026 00:06:08 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "3d6e8428fd4c7f76de9f87f77b2347f293109f4e88fb20c154b3fa34a7f687dd *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 20 May 2026 00:06:08 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 20 May 2026 00:06:08 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 20 May 2026 00:06:08 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 20 May 2026 00:06:08 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:1fbcdab7270278c1f989ae72190255d85d2117e990efb76cde6eb206b803672c`  
		Last Modified: Tue, 19 May 2026 22:36:02 GMT  
		Size: 48.4 MB (48379432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:859f1fd2278a31aad63f74ed3949f6c9a25aff4f9220c504caaf85e7428106e8`  
		Last Modified: Wed, 20 May 2026 00:06:34 GMT  
		Size: 144.7 MB (144724358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:093aaccee306ea5f9971ce53244946024f3b978efeee26c8bbbf87efaa738a14`  
		Last Modified: Wed, 20 May 2026 00:06:32 GMT  
		Size: 81.2 MB (81213624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:303d41b67697600e0e82cc6b00d34192a8f47ad8445bdfe8d53b9534938f786d`  
		Last Modified: Wed, 20 May 2026 00:06:29 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d62d1b0e4d5fbc46b73976e1a410d7f6570e8906ef2d6c03f2a42279bd3ae582`  
		Last Modified: Wed, 20 May 2026 00:06:28 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:c8baead859b7b8eb454edebaf42ca46bdc689ddd9d24c9939ce7bf0507733b75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7400762 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:650dcc70509bd18eb872519476b28c224571eed3633e8b5436dea48952fd8978`

```dockerfile
```

-	Layers:
	-	`sha256:2c331898c5aebfb589adc3a007e7a9c005c0aa380c066edd3f992d99547b987e`  
		Last Modified: Wed, 20 May 2026 00:06:29 GMT  
		Size: 7.4 MB (7384712 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:434d92519a27f1bf3d87abbb7ed8681766e86df0ef11929a3f38f33a855ab049`  
		Last Modified: Wed, 20 May 2026 00:06:28 GMT  
		Size: 16.1 KB (16050 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-bookworm` - linux; ppc64le

```console
$ docker pull clojure@sha256:d01724ded320c72757dc43b7d3aeeb781480fc67c00b5ab0ede7400a0aaf7759
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.2 MB (285154152 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:841942a08221ea66e37566751c9a51701e1503fa2f564f96f0290c9a73ee9123`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1779062400'
# Wed, 20 May 2026 05:54:25 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 20 May 2026 05:54:25 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 20 May 2026 05:54:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 May 2026 05:54:25 GMT
ENV CLOJURE_VERSION=1.12.5.1645
# Wed, 20 May 2026 05:54:25 GMT
WORKDIR /tmp
# Wed, 20 May 2026 05:58:07 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "3d6e8428fd4c7f76de9f87f77b2347f293109f4e88fb20c154b3fa34a7f687dd *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 20 May 2026 05:58:07 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 20 May 2026 05:58:07 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 20 May 2026 05:58:07 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 20 May 2026 05:58:07 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:b3943e183051423c3dc79fa53ad6d50fff9621945bbfc636eec039b14ead2b66`  
		Last Modified: Tue, 19 May 2026 22:35:10 GMT  
		Size: 52.3 MB (52340199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6633021a99f451d585b657cbca0d3fbc241ffb487dcadb3e2ad6afd10c777642`  
		Last Modified: Wed, 20 May 2026 05:55:35 GMT  
		Size: 145.8 MB (145766094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:626866d931c122e7a7d2e2f6828bf8f896c77cd664c345cbbb4961cd64b12640`  
		Last Modified: Wed, 20 May 2026 05:58:47 GMT  
		Size: 87.0 MB (87046819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:041d09845fc0c9fe029860e3835bc2c1a76d13e8323fffd56c388c335636c14a`  
		Last Modified: Wed, 20 May 2026 05:58:44 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97d831192f2e4477b2890421d84b7969a65fb60505fa5e7f3623dffc7b30ff39`  
		Last Modified: Wed, 20 May 2026 05:58:45 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:2339cbba08192cbb8d03196f9c0e0b140d49c7c742fa8d9a53ae4a33c464310b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7400145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7afc23f408c2637e589d98251297f473fb9fceae3fa2cd98a8377961af75ce19`

```dockerfile
```

-	Layers:
	-	`sha256:0f55fe93e177e2c9f6da87df8ab8eaae5dc1944819479bb54edd13a83dae073c`  
		Last Modified: Wed, 20 May 2026 05:58:45 GMT  
		Size: 7.4 MB (7384165 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2b1dc0cf8bb270c687ecbf67cff8c2e2a7d420504a81854c8df32f2e53e7be89`  
		Last Modified: Wed, 20 May 2026 05:58:44 GMT  
		Size: 16.0 KB (15980 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-bookworm` - linux; s390x

```console
$ docker pull clojure@sha256:be2c9ce22d6fe0979e1a8a2496c030ff770596b9c35fab2100b7e5c4457f314a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **263.1 MB (263092378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d036109d9ccc3e1ebace6d61efe1c9a3e3b3b11d1aba5fd16b467d319f72e08`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1779062400'
# Wed, 20 May 2026 01:43:28 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 20 May 2026 01:43:28 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 20 May 2026 01:43:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 May 2026 01:43:28 GMT
ENV CLOJURE_VERSION=1.12.5.1645
# Wed, 20 May 2026 01:43:28 GMT
WORKDIR /tmp
# Wed, 20 May 2026 01:44:39 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "3d6e8428fd4c7f76de9f87f77b2347f293109f4e88fb20c154b3fa34a7f687dd *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 20 May 2026 01:44:39 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 20 May 2026 01:44:39 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 20 May 2026 01:44:39 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 20 May 2026 01:44:39 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:e0fc2c7a6bb12f7a9b333cc117b6ea5fa5cf251c5fa4dd298303beee01028f59`  
		Last Modified: Tue, 19 May 2026 22:35:39 GMT  
		Size: 47.2 MB (47155589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c5e6deaec85cc5be451ebdae33f1ebb1ee8f8afce7f812c0687c0c3ed8574b1`  
		Last Modified: Wed, 20 May 2026 01:44:08 GMT  
		Size: 135.9 MB (135910432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:181f9c9f15ec012874fcee89590ca95021df6e015a8bff8bc2a1dc4feb280b2c`  
		Last Modified: Wed, 20 May 2026 01:45:05 GMT  
		Size: 80.0 MB (80025317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c77f6514ab060f224ed351e767f2447177d1d5ce4df78ce94983fef67df25ee3`  
		Last Modified: Wed, 20 May 2026 01:45:03 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:152e3d1dea4a2b5bfd183e41fc650b25f328ee9d2b4d6873086999ad89d84e03`  
		Last Modified: Wed, 20 May 2026 01:45:03 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:26ea9f71aaa09c7d926255619c8d60837f27a338a9bde1de7203772e35951dcb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7386200 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9acd8be209db1f26960355e01b71f6c5edfabdbfe00371e2907c2e5f7a7a8a10`

```dockerfile
```

-	Layers:
	-	`sha256:4ebd28c5af7c396c02444d29349686427f4f2f64aa9490b92205ab335d02136b`  
		Last Modified: Wed, 20 May 2026 01:45:03 GMT  
		Size: 7.4 MB (7370268 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bc28ffee38eb358477c29f23212724c94d54424fcbbe6b2473b5f02b7f14bc48`  
		Last Modified: Wed, 20 May 2026 01:45:03 GMT  
		Size: 15.9 KB (15932 bytes)  
		MIME: application/vnd.in-toto+json
