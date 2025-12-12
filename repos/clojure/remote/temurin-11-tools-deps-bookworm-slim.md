## `clojure:temurin-11-tools-deps-bookworm-slim`

```console
$ docker pull clojure@sha256:79a5ac20218dd4f9773adb9065f5ed4d278f99ff5c4d338f47b794edf1b3f5da
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

### `clojure:temurin-11-tools-deps-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:4a6ea2306a20c65ad5dfcd06db04172241e92b76abe264eb0c3a88d23aa76d15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.9 MB (242872966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8345e15f91c3fed0ab7b8d31906b782fdc92959d0bcf6ef6b0e9ccf72837ffa6`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1765152000'
# Thu, 11 Dec 2025 22:38:35 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Dec 2025 22:38:35 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 11 Dec 2025 22:38:35 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Dec 2025 22:38:35 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Thu, 11 Dec 2025 22:38:36 GMT
WORKDIR /tmp
# Thu, 11 Dec 2025 22:38:51 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 11 Dec 2025 22:38:51 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 11 Dec 2025 22:38:51 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:ae4ce04d0e1ccb5db08fa441b79635de5590399fae652d10bd3379b231be0ead`  
		Last Modified: Mon, 08 Dec 2025 22:17:22 GMT  
		Size: 28.2 MB (28228418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f704e60308ca0ba84d77a589e3e2c695dbad6a0dd52e8134951c02f0326bedc`  
		Last Modified: Thu, 11 Dec 2025 23:13:31 GMT  
		Size: 145.0 MB (144966599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8b1e3e541cf616399c4e177bdf7d12f4876c2151c3505ff016bcecd81a71f97`  
		Last Modified: Thu, 11 Dec 2025 22:39:27 GMT  
		Size: 69.7 MB (69677305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97261a7f7587463677903816aaf1e8a7a18f72a4398141ae070f159e6ec15190`  
		Last Modified: Thu, 11 Dec 2025 22:39:17 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:25f84c39305a78985d616140789c695ace0e813bb0086b5dff021705f6aaee86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5147796 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4dcccf35419414191d5445fb668b1f67f93b927ef540fd4dad300dc372aa5b3`

```dockerfile
```

-	Layers:
	-	`sha256:0f0ccba934a5091bb43920701a703fc747e63dfeed12490997a419dbfba22ac2`  
		Last Modified: Fri, 12 Dec 2025 01:35:12 GMT  
		Size: 5.1 MB (5133529 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3988541032a50f0f07cb9bc6d9aaeaba0f29f95a5d34982a56ce8c0fbddf8c3a`  
		Last Modified: Fri, 12 Dec 2025 01:35:13 GMT  
		Size: 14.3 KB (14267 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:b51b742561dbcff11f0c801b462e9eb3f0d66350f1c2bac1621bb0f82d4d93b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **239.4 MB (239393116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cae095210d4c686b068a9eb87bc99bae6190c827a0a51362250a190026eba91`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1765152000'
# Thu, 11 Dec 2025 22:38:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Dec 2025 22:38:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 11 Dec 2025 22:38:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Dec 2025 22:38:20 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Thu, 11 Dec 2025 22:38:20 GMT
WORKDIR /tmp
# Thu, 11 Dec 2025 22:38:35 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 11 Dec 2025 22:38:35 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 11 Dec 2025 22:38:35 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:8a4a7306158c2bef7a131de3110e384f4822829cbcce20bc6b4ba32dd82a1d87`  
		Last Modified: Mon, 08 Dec 2025 22:16:51 GMT  
		Size: 28.1 MB (28102229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9f2fa48ba914d6f6221b6a3df4d1e9e5cfac4718e0a15b5ec7aa364bd4347a7`  
		Last Modified: Thu, 11 Dec 2025 22:39:12 GMT  
		Size: 141.7 MB (141731551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71dd8578621a4f194729d8c88d2410dffa6091b6bf011e2a3a3e2976527043b7`  
		Last Modified: Thu, 11 Dec 2025 22:39:09 GMT  
		Size: 69.6 MB (69558690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90437fd94acf377d3b9ac6a6085ed01825b9ecee80a0f24c6436a76910453fe0`  
		Last Modified: Thu, 11 Dec 2025 22:39:03 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:7f201795724b5f6527b96fabdc40ece786501ed681490112643737d991acbaa8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5154293 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba9d183edf7c507de7c7626109a35eb772918805278630376fa4d82a79ebe0fb`

```dockerfile
```

-	Layers:
	-	`sha256:f643ac80d90b7f16c9836ebb1a48e2c652c707cb1c965b5c7c439499b41fb4dd`  
		Last Modified: Fri, 12 Dec 2025 01:35:19 GMT  
		Size: 5.1 MB (5139908 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1e6805458faeab3f94c6d96f8d7228cf9b12a595f9544491d5363e38e542f357`  
		Last Modified: Fri, 12 Dec 2025 01:35:19 GMT  
		Size: 14.4 KB (14385 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:a258f2531e92ae538602f8d1e6ca63886baa2f20b38106689c5c00a2cfff55ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **239.7 MB (239661522 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e72bfcdbaa37fc307148bbf6b8ecf7efdbd7d2f6aea893ffac68b2d085cc2e3a`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1765152000'
# Tue, 09 Dec 2025 16:17:15 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 09 Dec 2025 16:17:15 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 09 Dec 2025 16:17:15 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Dec 2025 16:17:15 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Tue, 09 Dec 2025 16:17:17 GMT
WORKDIR /tmp
# Thu, 11 Dec 2025 22:50:13 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 11 Dec 2025 22:50:16 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 11 Dec 2025 22:50:16 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:85c696326521b18996e4f030a7e27e2c57ad4956710f12ec3011da2c017e09ad`  
		Last Modified: Tue, 09 Dec 2025 09:15:52 GMT  
		Size: 32.1 MB (32068845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4470482a8eaaeab4dceb8ce35bb823da20ba2a67978f6a17163d36b3afe2763`  
		Last Modified: Tue, 09 Dec 2025 16:20:08 GMT  
		Size: 132.1 MB (132081995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7ed327483e2db9c7f805373164dcda71f1d7028e6df20f1e51b7c754b751441`  
		Last Modified: Thu, 11 Dec 2025 22:51:15 GMT  
		Size: 75.5 MB (75510038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f9c0891562495a9f4e39e819ae35edc59ef26bbaaa8ef12b72ca65f5bf9acf2`  
		Last Modified: Thu, 11 Dec 2025 22:51:07 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:edf2b7fee1cabcae7f2f8488bdf87e0a0d5e350277b037610c075e248ca3e62e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5152387 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc78035e74800e974058372336257f4623e71426029cd4735541fe952e0bf798`

```dockerfile
```

-	Layers:
	-	`sha256:786ce4711d330ec99e3bfc45a70d162c47b3822475acdedf30134884322852a5`  
		Last Modified: Fri, 12 Dec 2025 01:35:24 GMT  
		Size: 5.1 MB (5138072 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eccc1aa307c94c562e6c52269bf90f61953bb5b2ba22b3840fc412498c6c7bb3`  
		Last Modified: Fri, 12 Dec 2025 01:35:25 GMT  
		Size: 14.3 KB (14315 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-bookworm-slim` - linux; s390x

```console
$ docker pull clojure@sha256:40e58b0a68ba6409858132fd494f4373e4af4435fd90604df8a175166e4eae3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.1 MB (221066917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11a7bc0d56ea9bb344bc2c2c579b96c7443f3a2cae0284e75ee3da064cc909ae`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1765152000'
# Tue, 09 Dec 2025 01:26:21 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 09 Dec 2025 01:26:21 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 09 Dec 2025 01:26:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Dec 2025 01:26:21 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Tue, 09 Dec 2025 01:26:21 GMT
WORKDIR /tmp
# Thu, 11 Dec 2025 22:32:13 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 11 Dec 2025 22:32:14 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 11 Dec 2025 22:32:14 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:00a29f44cb5b31bbcf043ec5426ee1c018bb26435350712cb5e48d56c6d95792`  
		Last Modified: Mon, 08 Dec 2025 22:15:04 GMT  
		Size: 26.9 MB (26884429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38a89e0d855a144c8a937b507bba42121108ec2b59b7e013828e537deaaa8563`  
		Last Modified: Tue, 09 Dec 2025 01:27:18 GMT  
		Size: 125.7 MB (125694469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d45ea04e66ee6db9942031cfcd32e2e5bce811e278a41adc33d88b958a8038b2`  
		Last Modified: Thu, 11 Dec 2025 22:32:50 GMT  
		Size: 68.5 MB (68487374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3594e873d43ae407b2e2ba8780593f37e29061b3e66dc340120850d3b4dcfe5e`  
		Last Modified: Thu, 11 Dec 2025 22:32:43 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:88595f07d93f7b5226691694cba67744290d86b6b4f96a65fccb500c406df6e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5139120 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:538ddca9addd3ce3c0248893dd08b2e78c79442a7c1d3227994616ed9c37965c`

```dockerfile
```

-	Layers:
	-	`sha256:734b90f6bdf8c4062d8c7f4b9c7c98d73e611483a8a5e716626415b497465aef`  
		Last Modified: Fri, 12 Dec 2025 01:35:40 GMT  
		Size: 5.1 MB (5124854 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8c2be4132c4dddbc1acbcf224994391db4657d8ede668a4a2ac1c7b6bb48fc2b`  
		Last Modified: Fri, 12 Dec 2025 01:35:41 GMT  
		Size: 14.3 KB (14266 bytes)  
		MIME: application/vnd.in-toto+json
